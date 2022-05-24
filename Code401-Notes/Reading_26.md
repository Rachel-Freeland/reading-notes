# Reading for Class 26 -- Django
## Reading
 - [Getting Started with Django - Intro](https://www.djangoproject.com/start/)
 - [How Django works behind the scenes](https://wsvincent.com/how-django-works-behind-the-scenes/)

Django:
* Object-Relational Mapper - define data models entirely in Python
* URLs and views - To design URLs, create a Python module called URLconf. This file acts like a table of contents for 
  your app with a simple mapping between URL patterns and your views.
* Templates - designed to feel comfortable and easy to learn yet, it is flexible and highly extensible.
* Forms  - handles rendering forms as HTML, validating user-submitted data, and converting data to native Python types.
* Authentication - comes with a full-featured and secure authentication system allowing users to create accounts and to 
  safely log in and out.
* Admin - reads metadata in your models to provide a production ready interface that can be immediately used to start 
  managing content.
* Internationalization - full support for translating text into different languages plus, locale-specific formatting of 
  dates, times, numbers, and time zones.
* Security - provides protections against:
  * Clickjacking
  * XSS
  * CRSF
  * SQL injection
  * Remote code execution

### Bookmark & Review
- [What is Django?](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Introduction)
- [First Django App - Part I](https://docs.djangoproject.com/en/3.0/intro/tutorial01/)
- [First Django App - Part II](https://docs.djangoproject.com/en/3.0/intro/tutorial02/)

Django is a high-level python open source web framework that allows for rapid development of secure and maintainable 
websites. Django is considered a mildly opinionated framework. It provides a set of components to handle most tasks and 
1 of 2 preferred ways to implement them. Django applications group the code into separate files:
* URLs - processes every single URL via a single function. It utilizes a URL mapper to redirect HTTP requests to the 
  appropriate view.
* View - a request handler function... it receives HTTP requests and returns HTTP responses. This is done by the view 
  accessing the needed data via models and formatting the data via templates
* Models - an object that defines the structure of an app's data and allows for adding, modifying and deleting or 
  querying the data.
* Templates - a text file that defines the structure or layout of a file

Django also allows:
* Forms
* Authentication
* Caching
* Administration of a site
* Serializing data