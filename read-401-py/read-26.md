# DRF Permissions
*Authentication or identification by itself is not usually sufficient to gain access to information or code. For that, the entity requesting access must have authorization.*
![image](../img3/Permissions2.png)

Together with authentication and throttling, permissions determine whether a request should be granted or denied access.

Permission checks are always run at the very start of the view, before any other code is allowed to proceed. Permission checks will typically use the authentication information in the ```request.user``` and ```request.auth``` properties to determine if the incoming request should be permitted.

Permissions are used to grant or deny access for different classes of users to different parts of the API.

The simplest style of permission would be to allow access to any authenticated user, and deny access to any unauthenticated user. This corresponds to the ```IsAuthenticated``` class in REST framework.

A slightly less strict style of permission would be to allow full access to authenticated users, but allow read-only access to unauthenticated users. This corresponds to the ```IsAuthenticatedOrReadOnly``` class in REST framework.

### How permissions are determined

Permissions in REST framework are always defined as a list of permission classes.

Before running the main body of the view each permission in the list is checked. If any permission check fails an ```exceptions.PermissionDenied``` or ```exceptions.NotAuthenticated``` exception will be raised, and the main body of the view will not run.

When the permissions checks fail either a "403 Forbidden" or a "401 Unauthorized" response will be returned, according to the following rules:

- The request was successfully authenticated, but permission was denied. â€” An HTTP 403 Forbidden response will be returned.

- The request was not successfully authenticated, and the highest priority authentication class does not use ```WWW-Authenticate``` headers. â€” An HTTP 403 Forbidden response will be returned.

- The request was not successfully authenticated, and the highest priority authentication class does use ```WWW-Authenticate``` headers. â€” An HTTP 401 Unauthorized response, with an appropriate ```WWW-Authenticate``` header will be returned.

### Object level permissions

REST framework permissions also support object-level permissioning. Object level permissions are used to determine if a user should be allowed to act on a particular object, which will typically be a model instance.

Object level permissions are run by REST framework's generic views when ```.get_object()``` is called. As with view level permissions, an ```exceptions.PermissionDenied``` exception will be raised if the user is not allowed to act on the given object.

If you're writing your own views and want to enforce object level permissions, or if you override the ```get_object``` method on a generic view, then you'll need to explicitly call the ```.check_object_permissions(request, obj)``` method on the view at the point at which you've retrieved the object.

This will either raise a ```PermissionDenied``` or ```NotAuthenticated``` exception, or simply return if the view has the appropriate permissions.

### Limitations of object level permissions

For performance reasons the generic views will not automatically apply object level permissions to each instance in a queryset when returning a list of objects.

Often when you're using object level permissions you'll also want to filter the queryset appropriately, to ensure that users only have visibility onto instances that they are permitted to view.

### API Reference

The ```AllowAny``` permission class will allow unrestricted access, **regardless of if the request was authenticated or unauthenticated**.

This permission is not strictly required, since you can achieve the same result by using an empty list or tuple for the permissions setting, but you may find it useful to specify this class because it makes the intention explicit.

### IsAuthenticated

The ```IsAuthenticated``` permission class will deny permission to any unauthenticated user, and allow permission otherwise.

This permission is suitable if you want your API to only be accessible to registered users.

### IsAdminUser

The ```IsAdminUser``` permission class will deny permission to any user, unless ```user.is_staff``` is ```True``` in which case permission will be allowed.

This permission is suitable if you want your API to only be accessible to a subset of trusted administrators.

### IsAuthenticatedOrReadOnly

The ```IsAuthenticatedOrReadOnly``` will allow authenticated users to perform any request. Requests for unauthorised users will only be permitted if the request method is one of the "safe" methods; ```GET```, ```HEAD``` or ```OPTIONS```.

This permission is suitable if you want to your API to allow read permissions to anonymous users, and only allow write permissions to authenticated users.

### DjangoModelPermissions

This permission class ties into Django's standard ```django.contrib.auth``` model permissions. This permission must only be applied to views that have a ```.queryset``` property set. Authorization will only be granted if the user is authenticated and has the relevant model permissions assigned.

- ```POST``` requests require the user to have the ```add``` permission on the model.

- ```PUT``` and ```PATCH``` requests require the user to have the ```change``` permission on the model.

- ```DELETE``` requests require the user to have the ```delete``` permission on the model.

The default behaviour can also be overridden to support custom model permissions. For example, you might want to include a ````view``` model permission for ```GET``` requests.

To use custom model permissions, override ```DjangoModelPermissions``` and set the ```.perms_map``` property. Refer to the source code for details

### Using with views that do not include a ```queryset``` attribute.

If you're using this permission with a view that uses an overridden ```get_queryset()``` method there may not be a ```queryset``` attribute on the view. In this case we suggest also marking the view with a sentinel queryset, so that this class can determine the required permissions.

### DjangoModelPermissionsOrAnonReadOnly

Similar to ```DjangoModelPermissions```, but also allows unauthenticated users to have read-only access to the API.

### DjangoObjectPermissions

This permission class ties into Django's standard object permissions framework that allows per-object permissions on models. In order to use this permission class, you'll also need to add a permission backend that supports object-level permissions, such as django-guardian.

As with ```DjangoModelPermissions```, this permission must only be applied to views that have a ```.queryset``` property or ```.get_queryset()``` method. Authorization will only be granted if the user is authenticated and has the relevant per-object permissions and relevant model permissions assigned.

### Custom permissions

To implement a custom permission, override ```BasePermission``` and implement either, or both, of the following methods:

- ```.has_permission(self, request, view)```

- ```.has_object_permission(self, request, view, obj)```

The methods should return ```True``` if the request should be granted access, and ```False``` otherwise.

If you need to test if a request is a read operation or a write operation, you should check the request method against the constant ```SAFE_METHODS```, which is a tuple containing ```'GET'```, ```'OPTIONS'``` and ```'HEAD'```. For example:

Custom permissions will raise a ```PermissionDenied``` exception if the test fails. To change the error message associated with the exception, implement a ```message``` attribute directly on your custom permission. Otherwise the ```default_detail``` attribute from ```PermissionDenied``` will be used. Similarly, to change the code identifier associated with the exception, implement a ```code``` attribute directly on your custom permission - otherwise the ```default_code``` attribute from ```PermissionDenied``` will be used.

### Third party packages

The following third party packages are also available.

### DRF - Access Policy

The Django REST - Access Policy package provides a way to define complex access rules in declarative policy classes that are attached to view sets or function-based views. The policies are defined in JSON in a format similar to AWS' Identity & Access Management policies.

### Composed Permissions

The Composed Permissions package provides a simple way to define complex and multi-depth (with logic operators) permission objects, using small and reusable components.

### REST Condition

The REST Condition package is another extension for building complex permissions in a simple and convenient way. The extension allows you to combine permissions with logical operators.

### DRY Rest Permissions

The DRY Rest Permissions package provides the ability to define different permissions for individual default and custom actions. This package is made for apps with permissions that are derived from relationships defined in the app's data model. It also supports permission checks being returned to a client app through the API's serializer. Additionally it supports adding permissions to the default and custom list actions to restrict the data they retrieve per user.

### Django Rest Framework Roles

The Django Rest Framework Roles package makes it easier to parameterize your API over multiple types of users.

### Django REST Framework API Key

The Django REST Framework API Key package provides permissions classes, models and helpers to add API key authorization to your API. It can be used to authorize internal or third-party backends and services (i.e. machines) which do not have a user account. API keys are stored securely using Django's password hashing infrastructure, and they can be viewed, edited and revoked at anytime in the Django admin.

### Django Rest Framework Role Filters

The Django Rest Framework Role Filters package provides simple filtering over multiple types of roles.



## **_references:_**

**_read_**

1. [DRF Permissions](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)

1. [basics of hash tables](https://www.django-rest-framework.org/api-guide/permissions/)

1. [Classy Django REST](http://www.cdrf.co/)

1. [DRF Generic Views](https://www.django-rest-framework.org/api-guide/generic-views/)

**_vedio_**

1. [How to Use Django REST Framework Permissions](https://www.youtube.com/watch?v=yiYpFMk9QdA)

## Done

[home](../README.md) | [About me](../about-me.md) | [contact me](../contact-me.md)