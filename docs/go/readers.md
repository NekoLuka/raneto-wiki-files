---
Title: What are readers and how to use them
---

## What are readers and how to use them

A reader is a function that is able to modify a slice because
a slice is nothing more than a refrence to the underlying array.
It does this by taking the slice as a function param and returning
the length of the modified data and an error if one occurd.
Inside the function then the slice can be modified to fit the required behaviour.

### Example

```go
# This function fills the slice with only 'A'
func (r MyReader) Read(b []byte) (int, error) {
	for i := 0; i < len(b); i++ {
		b[i] = 'A'
	}
	return len(b), nil
}
```

### Links

Example: https://go.dev/tour/methods/21