# PostBoost Python SDK

Official Python client for the [PostBoost API](https://postboost.co/docs/api).

## Install

```bash
pip install postboost
```

| | |
|---|---|
| **PyPI** | [pypi.org/project/postboost](https://pypi.org/project/postboost/) |
| **GitHub** | [postboost-co/postboost-python](https://github.com/postboost-co/postboost-python) |
| **Docs** | [postboost.co/docs/api](https://postboost.co/docs/api) |
| **Version** | v1.0.0 |

## Quick start

```python
from postboost import ApiClient, Configuration, PostsApi

config = Configuration(access_token="YOUR_API_TOKEN")
with ApiClient(config) as client:
    api = PostsApi(client)
    posts = api.list_posts(workspace_uuid="YOUR_WORKSPACE_UUID")
    for post in posts:
        print(post.uuid)
```

## License

MIT
