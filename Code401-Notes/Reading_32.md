# Reading Notes for Day 32 - Permissions & Postgresql

## Reading
* [DRF Permissions](https://www.django-rest-framework.org/api-guide/permissions/)
<hr/>

* When combined with authentication and throttling, permissions determine whether a request should be granted or 
denied access.
* Permission checks are always run at the start of view before any other code is allowed to proceed.
* Permissions in REST framework are always defined as a list of permission classes.
* REST framework permissions support object-level permissioning.
* The default permission policy may be set globally, using the `DEFAULT_PERMISSION_CLASSES` setting.

```python
REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permissions.IsAuthenticated',
    ]
}
```

* If not specified, the default setting allows unrestricted access.
* Authentication can also be set on a per-view or per-viewset basis using the `APIView` class-based views.

### Bookmark & Review
* [Classy Django REST](https://www.cdrf.co/)
* [DRF Generic Views](https://www.django-rest-framework.org/api-guide/generic-views/)