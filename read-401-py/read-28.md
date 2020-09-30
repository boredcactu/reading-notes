# API Deployment

### Managing Django Settings: Issues

**Different environments**. Usually, you have several environments: local, dev, ci, qa, staging, production, etc. Each environment can have its own specific settings (for example: DEBUG = True, more verbose logging, additional apps, some mocked data, etc). You need an approach that allows you to keep all these Django setting configurations.

**Sensitive data**. You have SECRET_KEY in each Django project. On top of this there can be DB passwords and tokens for third-party APIs like Amazon or Twitter. This data cannot be stored in VCS.

**Sharing settings between team members**. You need a general approach to eliminate human error when working with the settings. For example, a developer may add a third-party app or some API integration and fail to add specific settings. On large (or even mid-size) projects, this can cause real issues.

**Django settings are a Python code**. This is a curse and a blessing at the same time. It gives you a lot of flexibility, but can also be a problem â€“ instead of key-value pairs, settings.py can have a very tricky logic.

### Setting Configuration: Different Approaches

There is no built-in universal way to configure Django settings without hardcoding them. But books, open-source and work projects provide a lot of recommendations and approaches on how to do it best. Letâ€™s take a brief look at the most popular ones to examine their weaknesses and strengths.

**settings_local.py**

This is the oldest method. I used it when I was configuring a Django project on a production server for the first time. I saw a lot of people use it back in the day, and I still see it now.

### 12 Factors

12 Factors is a collection of recommendations on how to build distributed web-apps that will be easy to deploy and scale in the Cloud. It was created by Heroku, a well-known Cloud hosting provider.

As the name suggests, the collection consists of twelve parts:

1. Codebase

1. Dependencies

1. Config

1. Backing services

1. Build, release, run

1. Processes

1. Port binding

1. Concurrency

1. Disposability

1. Dev/prod parity

1. Logs

1. Admin processes

Each point describes a recommended way to implement a specific aspect of the project. Some of these points are covered by instruments like Django, Python, pip. Some are covered by design patterns or the infrastructure setup. In the context of this article, we are interested in one part: the Configuration.

Its main rule is **to store configuration in the environment**. Following this recommendation will give us strict separation of config from code.


### django-environ

Based on the above, we see that **environment variables are the perfect place to store settings**.

Writing code using os.environ could be tricky sometimes and require additional effort to handle errors. Itâ€™s better to use django-environ instead.

Technically itâ€™s a merge of:

- envparse

- honcho

- dj-database-url

- dj-search-url

- dj-config-url

- django-cache-url

### Naming Conventions

Naming of variables is one of the most complex parts of development. So is naming of settings. We canâ€™t imply on Django or third-party applications, but we can follow these simple rules for our custom (project) settings:

- Give meaningful names to your settings.

- Always use the prefix with the project name for your custom (project) settings.

- Write descriptions for your settings in comments.

### Django Settings: Best practices

- Keep settings in environment variables.

- Write default values for production configuration (excluding secret keys and tokens).

- Donâ€™t hardcode sensitive settings, and donâ€™t put them in VCS.

- Split settings into groups: Django, third-party, project.

- Follow naming conventions for custom (project) settings.

### Conclusion

The Settings file is a small but very important part of any Django project. If you do it wrong, youâ€™ll have a lot of issues during all phases of development. But if you do it right, it will be a good basis for your project that will allow it to grow and scale in the future.

Using the environment variables approach, you can easily switch from a monolith to microservice architecture, wrap your project in Docker containers, and deploy it in any VPS or Cloud hosting platform such as: Amazon, Google Cloud, or your own Kubernetes cluster.

## **_references:_**

**_read_**

1. [Django Settings Best Practices](https://djangostars.com/blog/configuring-django-settings-best-practices/)

1. [SSH Tutorial](https://www.hostinger.com/tutorials/ssh-tutorial-how-does-ssh-work)

1. [White Noise](http://whitenoise.evans.io/en/stable/)

1. [IaaS](https://en.wikipedia.org/wiki/Infrastructure_as_a_service)

1. [PaaS](https://en.wikipedia.org/wiki/Platform_as_a_service)

1. [CORS](https://en.m.wikipedia.org/wiki/Cross-origin_resource_sharing)


**_vedio_**

1. [The 4 best ways to deploy a Django application](https://www.youtube.com/watch?v=IoxHUrbiqUo)

1. [Deploying a Django API to Heroku](https://www.youtube.com/watch?v=7-4je7mPjtU)

## Done

[home](../README.md) | [About me](../about-me.md) | [contact me](../contact-me.md)