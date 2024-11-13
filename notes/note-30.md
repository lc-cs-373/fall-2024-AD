# PLS Fall 2024 Note 30

## Types

Every expression has a type.  The type of a variable is the type that is bound
to the variable in the current type environment.  All variables must have a type
binding.

A type error is one of the following:

* an attempt to define a procedure whose declared return type does not match the
  type of the body of the procedure
* an attempt to apply a non-procedure as a procedure
* an attempt to apply a procedure to the wrong number of actual parameters
* an attempt to apply a procedure to actual parameters whose types do not match
  the declared types of the corresponding formal parameters
* an attempt to use a non-boolean as the test in an `if` statement
* an attempt to have expressions of different types in the `then` and `else`
  parts of an `if` statement
* an attempt to assign a value to a LHS variable in a `set` expression where the
  type of the variable does not match the type of the RHS expression

In the above, we consider primitive procedures such as `+`, `add1`, and `zero?`
as procedures for the purpose of type checking.