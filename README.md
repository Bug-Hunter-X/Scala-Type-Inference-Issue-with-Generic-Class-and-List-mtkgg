# Scala Type Inference Issue with Generic Class and List

This repository demonstrates a subtle issue with type inference in Scala when using a generic class with a List parameter.

The `MyClass` class is designed to hold a value of type `T`. When instantiating `MyClass` with an `Int`, `String`, or a `List`, there are some unexpected type inference issues.

The `bug.scala` file contains the buggy code.  The `bugSolution.scala` file provides a corrected version.  The issue is explained in the comments.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Compile and run `bug.scala` using the Scala compiler: `scalac bug.scala && scala MainObject`

You will observe an unexpected output or runtime error due to the unexpected List type inference.

## Solution

The solution is found in `bugSolution.scala` which explicitly sets the type to be `List[Int]` or `List[String]`