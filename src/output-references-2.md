# Output references

```aquascope,permissions,shouldFail,run
fn first_or(strings: &Vec<String>, default: &String) -> &String {
    if strings.len() > 0 {
        &strings[0]`{}`
    } else {
        default`{}`
    }
}
# fn main() {}
```
