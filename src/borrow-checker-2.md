# Borrow checker

<div style="font-size: 30px">

- By default data has only read/own permissions (@Perm{read}, @Perm{own})
- When annotated with `let mut` we win write permissions (@Perm{write})
- **References can _temporarily transfer_ these permissions**

</div>
