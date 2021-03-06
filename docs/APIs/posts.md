# Posts

## Index

Fetch paginated post list.

```
GET /api/v1/posts
```

```
params:

page: int | the page number of the paginated post list, default 1
```

```
Response:

{
    "data": [
        {
            "id": 1,
            "content": "...",
            "image": "http://localhost:8000/api/v1/images/1",
            "created_at": {
                "date": "2018-06-25 00:59:49.000000",
                "timezone_type": 3,
                "timezone": "UTC"
            }
        }
    ],
    "links": {
        "first": ".../api/v1/posts?page=1",
        "last": ".../api/v1/posts?page=1",
        "prev": null,
        "next": null
    },
    "meta": {
        "current_page": 1,
        "from": 1,
        "last_page": 1,
        "path": ".../api/v1/posts",
        "per_page": 20,
        "to": 1,
        "total": 1
    }
}
```

## Store

Create a post with content and image.

```
POST /api/v1/posts
```

```
Request:

{
	"content": "...",  // the content string you want to post, required
	"imageId": 1       // optional: the image id
}
```

```
Response:

{
    "data": {
        "id": 2,
        "content": "...",
        "image": "http://localhost:8000/api/v1/images/1",
        "created_at": {
            "date": "2018-06-24 19:56:05.000000",
            "timezone_type": 3,
            "timezone": "UTC"
        }
    }
}
```
