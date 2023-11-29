# Borrow checker

<div style="font-size: 30px">

Core idea: variables have three kinds of *permissions* on their data:

- **Read** (@Perm{read}): data can be copied to another location.
- **Write** (@Perm{write}): data can be mutated in-place.
- **Own** (@Perm{own}): data can be moved or dropped.

</div>
