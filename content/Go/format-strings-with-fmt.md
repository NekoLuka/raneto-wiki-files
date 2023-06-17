---
Title: Formatting a string in Go with fmt.Sprint()
---

## Formatting a string in Go with `fmt.Sprint()`

To format a string with custom data and return that string, you can use
`fmt.Sprint()` to accomplish this.

### Example

```go
func SayHi(name string) string {
    return fmt.Sprintf("Hi %s", name)
}
```

### Links

Format guide: https://pkg.go.dev/fmt#hdr-Printing  
Function refrence: https://pkg.go.dev/fmt#Sprintf