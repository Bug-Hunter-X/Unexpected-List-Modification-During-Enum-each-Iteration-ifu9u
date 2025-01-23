# Elixir List Modification During Enum.each
This example demonstrates an issue that arises when attempting to modify a list while iterating through it using `Enum.each`.  In Elixir, lists are immutable. Modifying them during iteration is not supported in the way one might expect from other languages.  The provided code illustrates this problem and offers a solution.

## Problem
The code attempts to remove the element `3` from a list during iteration. However, due to Elixir's immutability, this operation doesn't affect the original list. The `list = List.delete(list, x)` line creates a new list, but this doesn't change the list being iterated over.