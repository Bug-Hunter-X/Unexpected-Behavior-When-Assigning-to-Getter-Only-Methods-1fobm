# Unexpected Behavior When Assigning to Getter-Only Methods in Ruby

This repository demonstrates a common error in Ruby related to getter-only methods and assignment.  Assigning a value to a method that only defines a getter does not modify the object's internal state. This behavior is frequently unexpected, especially for those coming from languages with stricter property handling.

The `bug.rb` file illustrates the issue. The `MyClass` defines a getter for `@value` but lacks a setter. Attempting to assign a new value to `my_object.value` does not change the internal value of `@value`.

The `bugSolution.rb` file provides a solution showcasing the use of a setter method (using `attr_accessor` or defining a setter method explicitly) to correctly modify the object's state.