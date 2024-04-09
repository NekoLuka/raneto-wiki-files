---
Title: File-like objects
---

## What are file-like objects?
File like objects are python objects that have either a `.read()` or a `.write()` function.  
The most commonly known one is `open()` to read a file.  

## Different types of file-like objects
- `io.StringIO()`
- `io.BytesIO()`
- `open()`

## How to use?
### Convert BytesIO to str
```python
output_string = str(io_object.read().decode("utf-8"))
```
### Convert BytesIO to StringIO
```python
output_io_object = StringIO(io_object.read().decode("utf-8"))
```