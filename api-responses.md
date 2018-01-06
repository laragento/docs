# Api Responses

- [Introduction](#introduction)
- [Responses](#responses)

<a name="responses"></a>
## Responses
- Api responses from core modules are provided in json format. 

#### v1/category/33
``` json
{
  "data": {
    "id": 33,
    "category_id": 33,
    "name": "Küche",
    "parent_id": 2,
    "url_path": "kueche",
    [..]
  }
}
```

- When you request more details from a resource you will get the the base resource back
as well.
#### v1/category/33/children
``` json
{
  "data": {
    "id": 33,
    "category_id": 33,
    "name": "Küche",
    "parent_id": 2,
    "url_path": "kueche",
    [..],
    "children": {
      "data": Array[11][
        {
          "id": 7,
          "category_id": 7,
          "name": "Gewürze",
          "url_path": "kueche/gewuerze"
        },
        {
          "id": 8,
          "category_id": 8,
          "name": "Geschenke/Sets",
          "url_path": "kueche/geschenke"
        }
      ]
    }
  }
}
```