## 8.2 `object`

**Object**

This is the designation for singleton classes. These are also classes that have exactly one instance. You can't create a new instance of an "object" with this name, because it already exists and is defined at its declaration.

## 8.2.1 Global `object`

It's easy to forget the name of some global function. That's why it's sometimes useful to put these functions into one object.

Create `Network` **object** in a separate `.kt` file, where you will define configuration values and functions for your application.

In this object, create:
- Private variable `BASE_URL` with value `"https://dummyjson.com/"`
- Private constant `TIMEOUT` with value `5000`
- Public function `setBaseUrl(path: String)`, which sets `BASE_URL` if it's valid (starts with "https://.../")
- Public function `get(path: String)`, which returns a URL composed of `BASE_ULR + path`

Test the functionality and usage of this object.

## 8.2.2 Interface as argument 2

Modify the task [7.7.3 Interface as argument](../07-oop-basics/07-07-interface.MD) so you don't implement `HttpListener` as a separate class, but try to use an **object**:

```kt
fun main() {
    invoke(
        "https://api.ipify.org/?format=json",
        object : HttpListener {
            // ...
        })
}
```

This way, you can define different behavior for each call to the `invoke` function without creating new classes.