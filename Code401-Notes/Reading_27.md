# Reading Day 27 --> Django Models

## Reading
- [Using Models](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Models)
- [Django Admin](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Admin_site)

* Django web apps access data through objects known as ***models***. 
* Models define the structure of the data.
* Use separate models for each object.
* Models can define selection-list options
* Defined in the `models.py` folder and implemented as a subclass of `django.db.models.Model`
* Can contain fields, methods, and metadata.
```python
from django.db import models
from django.urls import reverse
class MyModelName(models.Model):
    """
    A typical class string defining a model, derived from the Model class.
    """
    # Fields
    my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')
    
    # Metadata
    class Meta:
        ordering = ['-my_field_name']
    
    # Methods
    def get_absolute_url(self):
        """
        Returns the URL to access a particular instance of MyModelName.
        """
        return reverse('model-detail-viw', args=[str(self.id)])

    def __str__(self):
        """
            String for representing the MyModelName object (in Amin site etc...)
        """
        return self.my_field_name
```


* Each field represents a column of data that we want to store in the database tables.


### Optional
- [Beginner's Guide to Django - Part I](https://simpleisbetterthancomplex.com/series/2017/09/04/a-complete-beginners-guide-to-django-part-1.html)

#### Bookmark & Review
- [Beginner's Guide to Django - Part II](https://simpleisbetterthancomplex.com/series/2017/09/11/a-complete-beginners-guide-to-django-part-2.html)

