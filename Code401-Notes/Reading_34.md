# Day 34 of Reading Notes --> API Deployment

## Reading
* [Django Settings Best Practices](https://djangostars.com/blog/configuring-django-settings-best-practices/)
* [SSH Tutorial](https://www.hostinger.com/tutorials/ssh-tutorial-how-does-ssh-work)
<hr/>

* `settings_local.py` -> used when configuring Django project on production server
  * Pros:
    * Secrets are not in VCS
  * Cons:
    * You can lose some of your Django environment settings because, this file is not in the VCS
    * This file can contain some non-obvious logic
    * Requires a `settings_local.example` for the VCS to share the default configs for other devs
* Create a settings file for each environment -> an extension of the `settings_local.py` approach
  * Make a ***settings/*** package
  * ```text
    settings/
        __init__.py
        local.py
        base.py
        ci.py
        local.py
        settigns.py
        production.py
    ```
  * Pros:
    * All environments are in VCS
    * Easy to share setting between devs
  * Cons:
    * Still need to figure out a way to handle secret passwords and tokens
    * Inheritance of settings can be hard to trace and maintain
* Sensitive data can be stored in Environment Variables
  * Use `import os`
  * ```python
    import os  
    
    def get_env_value(env_variable):
        try:
            return os.environ[env_variable]
        except KeyError:
            error_msg = 'Set the {} environment variable'.format(var_name)
            raise ImproperlyConfigured(error_msg)

    SECRET_KEY = os.environ['SECRET_KEY']
    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.postgresql',
            'NAME': os.environ['DATABASE_NAME'],
            'HOST': os.environ['DATABASE_HOST'],
            'PORT': int(os.environ['DATABASE_PORT']),
        }
    }
    ```

  * Pros:
    * Config is seperated from code
    * You have the same code for all environments
    * No inheritance settings, and cleaner and more consistent code
    * See 12 Factors 
  * Cons;
    * You still need to handle sharing default configs between devs
* 12 Factors -> a collection of recommendations on how to build distributed web apps. Created by Heroku:
  1. Codebase
  2. Dependencies
  3. Config
  4. Backing services
  5. Build, Release, Run
  6. Processes
  7. Port Binding
  8. Concurrency
  9. Disposability
  10. Dev/Prod parity
  11. Logs
  12. Admin processes
  * Each point describes a recommended way to implement specific aspects of a project
  * [12 Factors](https://12factor.net/)

### Bookmark & Review
* [White Noise](http://whitenoise.evans.io/en/stable/)
* [IaaS](https://en.wikipedia.org/wiki/Infrastructure_as_a_service)
* [PaaS](https://en.wikipedia.org/wiki/Platform_as_a_service)
* [CORS](https://en.m.wikipedia.org/wiki/Cross-origin_resource_sharing)