# Reading Day 28 --> Django CRUD and Forms

## Reading
* [Django Forms](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms)

* The role of the server is to first render the initial state of the form.
* After the user hits submit, the server will receive the form data from the browser and then, must validate it.
* In Django, the view gets a request then, performs any actions required including, reading data from the models then, 
  generates and returns an HTML page.
  1. Display the default form the 1<sup>st</sup> time it is requested by the user.
     1. The form is referred to as "unbound" at this time.
  2. Receive data from a `submit` request and bind it to the form data
  3. Clean and validate the data
     1. This means, removing invalid characters that might be used to send malicious content to the server and converts 
        it to consistent Python types.
     2. Checks that the values are appropriate for the fields.
  4. If any data is invalid, redisplay the form with any user populated values and the corresponding error messages.
  5. If all data is valid, perform the required actions
  6. Once all is complete... redirect the user to another page
* Declaring a form is much like declaring a Model.
* Easiest way to validate a single field is to override the method `clean_<fieldname>()`
```python
import datetime
from django import forms

from django.core.exceptions import ValidationError
from django.utils.translation import gettext_lazy

class RenewBookFrom(forms.Form):
    renewal_date = forms.DateField(help_text="Enter the date between now and 4 weeks (default 3)")

    def clean_renewal_date(self):
        data = self.cleaned_data['renewal_date']

        if data < datetime.date.today():
            raise ValidationError(_('Invalid date - renewal in the past'))
        if datetime > datetime.date.today() + datetime.timedelta(weeks=4):
            raise ValidationError(_('Invalid date - renewal more than 4 weeks ahead'))
        return data
```

### Bookmark & Review
* [Django Templates](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Home_page)
* [Django Views](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Generic_views)