# Files.Models.Style

## Example Style Object

```
{
  "id": 1,
  "path": "example",
  "logo": "https://mysite.files.com/...",
  "thumbnail": {
    "name": "My logo",
    "uri": "https://mysite.files.com/.../my_image.png"
  }
}
```

* `id` / `id`  (int64): Style ID
* `path` / `path`  (string): Folder path. This must be slash-delimited, but it must neither start nor end with a slash. Maximum of 5000 characters.
* `logo` / `logo`  (image): Logo
* `thumbnail` / `thumbnail`  (image): Logo thumbnail
* `file` / `file`  (file): Logo for custom branding.


---

## Show Style

```
Style style = Style.find(
    String path, 
    HashMap<String, Object> parameters = null,
    HashMap<String, Object> options = null
)
```

### Parameters

* `path` (String): Required - Style path.


---

## Update Style

```
Style style = Style.update(
    String path, 
    HashMap<String, Object> parameters = null,
    HashMap<String, Object> options = null
)
```

### Parameters

* `path` (String): Required - Style path.
* `file` (byte[]): Required - Logo for custom branding.


---

## Delete Style

```
void style = Style.delete(
    String path, 
    HashMap<String, Object> parameters = null,
    HashMap<String, Object> options = null
)
```

### Parameters

* `path` (String): Required - Style path.


---

## Update Style

```
Style style = Style.find(path);

HashMap<String, Object> parameters = new HashMap<>();
parameters.put("file", "file");

style.update(parameters);
```

### Parameters

* `path` (String): Required - Style path.
* `file` (byte[]): Required - Logo for custom branding.


---

## Delete Style

```
Style style = Style.find(path);

HashMap<String, Object> parameters = new HashMap<>();

style.delete(parameters);
```

### Parameters

* `path` (String): Required - Style path.
