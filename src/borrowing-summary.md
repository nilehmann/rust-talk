# Summary

<div style="font-size: 30px">

- All variables can read (@Perm{read}), own (@Perm{own}), and (optionally) write (@Perm{write}) their data.
- Creating a reference will transfer permissions from the borrowed path to the reference.
- Permissions are returned once the reference's lifetime has ended.
- Data must outlive all references that point to it.

</div>
