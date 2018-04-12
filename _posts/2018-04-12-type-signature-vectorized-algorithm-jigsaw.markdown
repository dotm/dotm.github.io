---
layout: post
title: "Type signature, vectorized ML algorithm, and jigsaw puzzle [Technical Tips]"
---

There's this interesting technique to find or create function by only looking at the inputs and the outputs of that function. I'd call this technique the Jigsaw Technique, but I'm still open for a better name for this technique (and a better title for this post). Let me elaborate on this technique (TL;DR is at the end).

Say you want a function. You have a Monad and an input function (that takes a normal value and return a Monad) as input. And you want to find a higher order function that applies that input function to element(s) inside the Monad. How do you do that?

Well, first let's write out the type signature of the inputs:
-	The Monad will have type: Monad input_monad
  - or in Haskell: Monad m => m a
-	The input function will have this type signature: normal_value -> Monad output_monad
  - or in Haskell: Monad m => (a -> m b)
Then we write the type signature of the desired output:
-	The resulting output will have type: Monad result_monad
  - or in Haskell: Monad m => m b

So, this function we want to find will have the type signature: Monad m => m a -> (a -> m b) -> m b

It takes 'm a' (the monadic input value) and the function '(a -> m b)' (which takes a normal value and output a monadic value), and use both output to create another monadic value 'm b'.

If you search 'Monad m => m a -> (a -> m b) -> m b' at Hoogle, you'll find that the >>= function have exactly that type signature. And lucky you, that >>= function does exactly what you want: applies an input function to element(s) inside the Monad.

Sometimes, you won't be so lucky. Sometimes you'll find two or more functions that have the type signatures you're looking for, and then you'll have to read the body of those functions until you find one that exactly match your requirement.

Sometimes, you'll even be less lucky and you won't find that function to be built-in, and you'll need to write it yourself. Even in such times, you'll find that knowing the type signatures of the inputs and outputs will help you write the function body by giving you hints on how to transform the inputs little-by-little until you have the desired outputs.

Now, let's move to Machine Learning. Some algorithms for Machine Learning (linear regression, logistic regression, etc.) can be implemented using for loop or using matrix and vector operations. Using matrix and vector operations to implement the algorithm is called vectorizing the algorithm. 

The difference in performance between vectorized and non-vectorized algorithm is not laughable. I once run both vectorized and non-vectorized implementation of a multi-class classification problem using logistic regression. The non-vectorized run for about 5 minutes and the vectorized one takes only about 15 seconds.

So how do you write an algorithm using matrix and vector operators (and not using loop)? How do you translate the formula of logistic regression into a vectorized algorithm (which use sigma notation and hence easier to translate to loop)?

Well, you can try to translate each sigma into matrix and vector operation by looking at the definitions of each operation. For example, the dot product of two vectors is the sum of element-wise multiplication of the two vectors. And, the matrix multiplication is... Well you know how complex matrix multiplication is.

An easier way is to use the Jigsaw Technique. But, this time, instead of looking at type signatures, we'll be looking at matrix (or vector) dimensions.

For example, say you have a 10-class classification problem and you want to predict the result of some training examples once you have calculates the appropriate theta/parameters.

You have two inputs. One input is a matrix X containing 5000 training example (m=5000) with 401 features including the intercept feature (n+1 = 401). So this matrix will have the dimension of 5000 by 401. The second input is the theta matrix with the dimension of 10 by 401 (10 is the 10 possible class of an example and 401 is all the features including the intercept feature).

The output we want is to label all the 5000 training example with the appropriate label from the potential 10-class label. So the output will have the dimension of 5000 by 1 (1 since we'll only be giving the highest prediction probability).

Let's use the Jigsaw Technique to (magically) create this function.

X is 5000 by 401
Theta is 10 by 401

Applying theta will results in the predictions of each training example to all potential class. To apply it we just look at the dimension of X and theta. We see a mismatch if we want to apply matrix multiplication, but that can be remedied by transposing one of them. Which one do we transpose? Well since the end result will have 5000 by 1 dimension, it's probably better to not transpose the X, since the X has that 5000 as row.

Theta^(T) is 401 by 10
Prediction = X * Theta^(T)
Prediction is 5000 by 10

Now we just have to get the index of the maximum value of each 5000 row of training example.

That's it.
We don't have to worry about translating the sigma notation of the formula bit-by-bit into matrix multiplication. We just look at the input dimensions, look at the output dimensions, do the appropriate transpose and multiply them. And, BOOM, by the power of magic we get the correct result.

TL;DR. The essence of Jigsaw Technique is this. We have 3 adjacent pieces of jigsaw puzzle (ooo). The inputs collectively represent one piece of the puzzle (o--). The outputs collectively represent another piece (--o). You want to find the correct middle piece (-o-) that will take you from the inputs to the outputs. What you do is just look at the shape of the left and the right piece, and you'll have an easier time getting the correct middle piece.
