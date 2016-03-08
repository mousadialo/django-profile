# Extend the Registration Form #

# Introduction #

Sometimes you just want to use the provided registration form, but sometimes you want to extend it, like adding a field, which for instance  can be saved in the profile.

Since [revision 432](https://code.google.com/p/django-profile/source/detail?r=432) it's possible.

# Details #

Imagine you create a profile with a field `gender`.

In `myapp/models.py` :
```
from userprofile.models import BaseProfile

GENDER_CHOICES=(('m', 'mam'), ('f', 'woman'))

class Profile(BaseProfile):
  gender = models.CharField(max_length=1, choices=GENDER_CHOICES)
```

In your `settings.py` you have :
```
AUTH_PROFILE_MODULE="myapp.profile"
```

Now you must extend the original `RegistrationForm` to add your field :

In `myapp/forms.py`:
```
from userprofile.forms import RegistrationForm
from myapp.models import GENDER_CHOICES

class MyRegistrationForm(RegistrationForm):
  gender = models.CharField(widget=forms.RadioSelect(choices=GENDER_CHOICES))

  def save(self, *args, **kwargs):
    user = super(MyRegistrationForm, self).save(*args, **kwargs)
    try:
      profile = user.get_profile()
    except:
      profile = Profile(user=user)
    profile.gender = self.cleaned_data['gender']
    profile.save()
```

And then add in your `settings.py` :
```
REGISTRATION_FORM = "myapp.forms.MyRegistrationForm"
```

And that's it, the form will be adapted to your needs.

You can do this even if you don't have new fields but for automatically create the profile when the user is created.