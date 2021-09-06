#  Permissions & Postgresql


## Permissions

**Authentication or identification by itself is not usually sufficient to gain access to information or code. For that, the entity requesting access must have authorization.**


## How permissions are determined

**Permissions in REST framework are always defined as a list of permission classes.**

***Before running the main body of the view each permission in the list is checked. If any permission check fails an exceptions.PermissionDenied or exceptions.NotAuthenticated exception will be raised, and the main body of the view will not run.***

> When the permissions checks fail either a "403 Forbidden" or a "401 Unauthorized" response will be returned, according to the following rules:

- **The request was successfully authenticated, but permission was denied. — An HTTP 403 Forbidden response will be returned.**

- **The request was not successfully authenticated, and the highest priority authentication class does not use WWW-Authenticate headers. — An HTTP 403 Forbidden response will be returned.**

> **The request was not successfully authenticated, and the highest priority authentication class does use WWW-Authenticate headers. — An HTTP 401 Unauthorized response, with an appropriate WWW-Authenticate header will be returned.**


## Object level permissions

REST framework permissions also support object-level permissioning. Object level permissions are used to determine if a user should be allowed to act on a particular object, which will typically be a model instance.

Object level permissions are run by REST framework's generic views when .get_object() is called. As with view level permissions, an exceptions.PermissionDenied exception will be raised if the user is not allowed to act on the given object.

If you're writing your own views and want to enforce object level permissions, or if you override the get_object method on a generic view, then you'll need to explicitly call the .check_object_permissions(request, obj) method on the view at the point at which you've retrieved the object.

This will either raise a PermissionDenied or NotAuthenticated exception, or simply return if the view has the appropriate permissions.

## API Reference

### 1-AllowAny

***The AllowAny permission class will allow unrestricted access, regardless of if the request was authenticated or unauthenticated.***

### 2-IsAuthenticated


***The IsAuthenticated permission class will deny permission to any unauthenticated user, and allow permission otherwise.***

***This permission is suitable if you want your API to only be accessible to registered users.***

### 3-IsAdminUser

***The IsAdminUser permission class will deny permission to any user, unless user.is_staff is True in which case permission will be allowed.***


### 4-IsAuthenticatedOrReadOnly

***The IsAuthenticatedOrReadOnly will allow authenticated users to perform any request. Requests for unauthorised users will only be permitted if the request method is one of the "safe" methods; GET, HEAD or OPTIONS.***


# DjangoModelPermissions

***This permission class ties into Django's standard django.contrib.auth model permissions. This permission must only be applied to views that have a .queryset property or get_queryset() method. Authorization will only be granted if the user is authenticated and has the relevant model permissions assigned.***


- **POST** requests require the user to have the add permission on the model.

- **PUT** and PATCH requests require the user to have the change permission on the model.

- **DELETE** requests require the user to have the delete permission on the model.







