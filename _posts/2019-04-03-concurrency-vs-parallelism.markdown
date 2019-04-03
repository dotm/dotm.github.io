---
layout: post
title: "Concurrency vs Parallelism"
---

## 3 tasks:
```
-A-A-A-|
-B-B-B-|
-C-C-C-|
```

## Serial vs. Parallel
Serial (one processor):
```
-A-A-A-B-B-B-C-C-C-|
```
Parallel (multiple processors):
```
-A-A-A-|
-B-B-B-|
-C-C-C-|
```

## Sequential vs Concurrent
Sequential (one task in progress at any time):
```
-A-A-A-B-B-B-C-C-C-|
```
Concurrent (multiple tasks in progress at any time):
```
-A-B-C-A-B-C-A-B-C-|
```