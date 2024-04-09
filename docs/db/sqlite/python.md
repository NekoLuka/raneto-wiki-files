---
Title: How to use sqlite3 in Python
---

## Thread safety
To turn off thread safety use the following initialization function. Use this when creating a multi-threaded application.
You do however need to watch out for conflicts when writing to the DB. Consider using some kind of [lock](#simple-db-write-lock).
```python
con = sqlite3.connect("my.db", check_same_thread=False)
```

## Simple DB write lock
This is a simple example of a DB write lock for sqlite3. DON'T USE FOR PRODUCTION CODE!
```python
class Lock:
    def __init__(self, cursor):
        self.cursor = cursor
        self.lock = False
    
    def obtain_cursor(self):
        while True:
            if self.lock == False:
                self.lock = True
                return self.cursor
    
    def release_cursor(self):
        self.lock = False
```
By using this class, functions will wait for one another to finish their turn with the cursor.