# Why are Forms Useful?

Django also makes form creation and handling form information a breeze.

When surfing the internet, you’re constantly interacting with forms and
you might not even realize it!

Looking something up on a search engine? Signing up for a new account?
Logging in? Ordering from your favorite restaurant? These applications
all use forms one way or another. Typically these forms are all written
in HTML, but with Django and *DTL* you can create forms even quicker and
suited for your needs.

# Forms

## What are Forms?

When working in most application, user information is gathered using
*forms*. Forms are mostly different input fields asking unique
questions. Data gathered from forms is usually used later in the backend
of the application.

In Django, these forms look and act generally the same as normal HTML
forms. The largest difference between Django forms and HTML forms is
that Django uses a model based system to handle the data. More
information can be found in
<a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank" rel="noopener">MDN’s HTML forms documentation</a>.

When creating forms in Django, we have a number of different options
available in regards to building the form. In this lesson, we’ll go over
some of these methods. Including one that allows Django to build the
form for us, reducing the amount of HTML we have to write ourselves.



<img alt="Image of a website called 'Goooble' that resembles Google search engine. There is a search form and the text inside says, &quot;Is this search bar a form?&quot;

" src="https://content.codecademy.com/courses/learn-html-forms/search%20bar.gif" class="gamut-1h2re45-imageStyles-imageStyles e1xtjyf0">

## An Overview of HTML Forms

When a form is created in any HTML document, the `<form>` element is
used to tell the application where the user input will come from. This
<a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank" rel="noopener"><code
class="code__2rdF32qjRVp7mMVBHuPwDS">&lt;form&gt;</code> element</a> has
two main attributes, `action` and `method`.

`action` is used to tell the application what script to run when the
form is submitted. Most forms need an `action` attribute, but we don’t
need it since Django handles the form submission for us.

`method` is used to tell the application where to submit the form data.
For Django, this attribute is optional and has two possible values,
`"POST"` and `"GET"`. `"POST"` requests will send information to the
server, while `"GET"` requests will retrieve information. We’ll be using
`"POST"` for form submission.

Inside of the `<form>` can be a number of different elements. The two
we’ll go over right now are the `<input>` and `<label>` elements. The <a
href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank" rel="noopener"><code
class="code__2rdF32qjRVp7mMVBHuPwDS">&lt;label&gt;</code> element</a> is
used to add a label to the `<input>` element. And the <a
href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank" rel="noopener"><code
class="code__2rdF32qjRVp7mMVBHuPwDS">&lt;input&gt;</code> element</a> is
where the user will input data for the form.

The `<input>` element has a number of optional attributes. Some of those
being the `id` and `name` attributes. The `name` attribute is used to
help us grab the data from the form in our Django application. The `id`
attribute is used for identifying and referencing specific HTML
elements. This is usually used later for the `for` attribute value in a
`<label>`.

An important attribute that is used with the `<input>` element is the
`type` attribute. This is used to tell the HTML document what data types
to accept for input. For instance, if we use the type `"email"`, the
form will not submit unless an email is typed into the input field.

Once all the necessary input elements are added to the form, one more
`<input>` element is needed that is of type `"submit"`. This will create
a button that lets the user send their data to the application once all
of the fields are filled out.

There’s a lot more that we can explore for HTML forms, but we’ll see
later on how Django takes care of some of this work for us.



**1.**

Create a `<form>` element to the HTML document currently open
(**owner_create_form.html**). Set the `action` to `""` and the `method`
to `"POST"`.





**2.**

Inside of `<form>`, create a `<label>` element with:

-   a `name` attribute set as `"LabelField"`,
-   a `for` attribute set as `"InputField"`.
-   the text of the `<label>` to `Owner name:`.





**3.**

Add the `<input>` element after the `<label>` element. Set both `name`
and `id` as `"InputField"`.





**4.**

At the bottom of the form, add an `<input>` with `type` as `"submit"`
that also has a `value` of `"Submit"`.







```html
<form action="" method="POST">
  <label name="LabelField" for="InputField">Owner Name:</label>
  <input id="InputField" name="InputField"/>
  <input type="submit" value="Submit"/>
</form>
```

## Form Security

When building any online form, proper defenses need to be made to
protect the application from any malicious users. This is because any
form is susceptible to attacks including *Cross Site Request Forgery*
attacks, or *CSRF* attacks. These attacks happen when a user uses
another user’s credentials without their knowledge and executes
malicious actions.

Django has a built in method for defending against CSRF attacks by
including a *<a href="https://docs.djangoproject.com/en/3.1/ref/csrf/"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank" rel="noopener">CSRF token</a>*. The CSRF token protects
the application and the user by adding a secret token inside of the
`"POST"` methods in the forms each time the form is rendered. The CSRF
token ensures that only the proper user is using the proper credentials.

The best way to add this token is to add a tag to the template inside of
the `<form>` element:

```html
<form>
  {% csrf_token %}
  ...
</form>
```

This token adds all the necessary security to help defend from possible
CSRF attacks and is conventionally placed at the beginning of the form.

Form validation is also necessary to help defend out applications from
possible attacks that use incorrect data types to cause problems, e.g.
<a href="https://www.w3schools.com/sql/sql_injection.asp"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank" rel="noopener">SQL attacks</a>. This validation can
include ensuring only specific data types are being submitted to protect
our database.

Form validation is usually done in **views.py** in Django, and consists
of an `if` statement before assigning data from the form to the
database:

```python
if form.is_valid():
  form = form.save()
```

Notice how Django makes it easy to secure our application!



**1.**

Add a CSRF token to the under the opening `<form>` declaration like in
the example given above.





**2.**

In **views.py** there is a method called `OwnerCreate(request)`. Inside
of that method, locate the line `form = OwnerCreateForm(request.POST)`
and add your validation below it and save the form if the form is valid.

**Note**: There is some extra code within this method that you may not
recognize, but don’t worry, we’ll be covering this code later!







```html
<form action="" method="POST">
  <!-- Add your token below-->
  {% csrf_token %}
  <label name="LabelField" for="InputField">Owner Name:</label>
  <input name="InputField" id="InputField"/>
  <input value="Submit" type="submit"/>
</form>
```

```python
from django.shortcuts import render
from django.views.generic import ListView
from django.views.generic.edit import CreateView, DeleteView, UpdateView

from .models import Owner
from .forms import OwnerCreateForm

pets = [
  { "petname": "Fido", "animal_type": "dog"},
  { "petname": "Clementine", "animal_type": "cat"},
  { "petname": "Cleo", "animal_type": "cat"},
  { "petname": "Oreo", "animal_type": "dog"},
]

def home(request):
  context = {"name": "<Put your name here>", "pets": pets}
  return render(request, "vetoffice/home.html", context)

class OwnerList(ListView):
  model = Owner

def OwnerCreate(request):
  if request.method == "POST":
    form = OwnerCreateForm(request.POST)
    # Add the form validation below:
    if form.is_valid():
      form = form.save()
  else:
    form = OwnerCreateForm()
  return render(request, "vetoffice/owner_create_form.html", {"form":form})
```

## Submitting a Form

In Django, we’ll be using the `"POST"` method when the form is
submitted, which means all of the data from the forms will be sent to
the POST method in **views.py**.

Before we go into accessing the POST data, we need to understand that
the logic is stored in the same function in **views.py** that renders
the template. Therefore, to differentiate how the view function should
treat a POST request vs rendering the usual form, we use an `if`
statement. This `if` statement checks that the request method is
`"POST"`. Here’s an example for how to structure our view function that
handles the rendering logic:

```python
from .models import Model_Name
 
def renderTemplate(request):
  if request.method == "POST":
    test_model = Model_Name()
    test_model.field = request.POST["field_name"]
    test_model.save()
  return render(request, "template_with_form.html")
```

The first thing that needs to be done is to check if the
`request.method` is equal to `"POST"`. When the method is `"POST"`, it
means that the form was submitted which means that we can grab all the
data and use it to create a new model instance. Notice our `test_model`
is a `new Model_Name()`. We then assign the `test_model.field` a value
of `request.POST["field_name"]`. This is because in our form, we had an
input field with a `name` set to `"field_name"`. The
`request.POST["field_name"]` syntax shows that `request` is treated like
a dictionary with a `"field_name"` property. Once all of the data from
`request.POST` is added to the model, we can save the model and render
the form again.

If our conditional isn’t met, it usually means that the form is being
rendered for the first time, so we can skip the instance creation and
just render the form as normal.

Aside from re-rendering the template, we could also redirect to a new
template! We’ll discuss redirecting in more detail later.



**1.**

In **views.py**, locate the method `OwnerCreate()` and add an `if`
statement to check if the request method is `"POST"`.





**2.**

If the method is `"POST"`, create a new instance called `newOwner` using
the `Owner` model.





**3.**

Access `"first_name"` from `POST` and assign it to
`newOwner.first_name`. Do the same thing for `last_name` and
`phone_number`. Once that’s done, save the model.







```python
from django.shortcuts import render
from django.views.generic import ListView
from django.views.generic.edit import CreateView, DeleteView, UpdateView

from .models import Owner
from .forms import OwnerCreateForm

pets = [
   { "petname": "Fido", "animal_type": "dog"},
   { "petname": "Clementine", "animal_type": "cat"},
   { "petname": "Cleo", "animal_type": "cat"},
   { "petname": "Oreo", "animal_type": "dog"},
]

def home(request):
   context = {"name": "Djangoer", "pets": pets}
   return render(request, "vetoffice/home.html", context)

class OwnerList(ListView):
   model = Owner

def OwnerCreate(request):
  # Add your code below:
  if request.method == "POST":
    newOwner = Owner()
    newOwner.first_name = request.POST["first_name"]
    newOwner.last_name = request.POST["last_name"]
    newOwner.phone_number = request.POST["phone_number"]
    newOwner.save()
  return render(request, "vetoffice/owner_create_form.html")
```

## Generics in Django: forms.py

Django can also help streamline the form creation process for us! We
first need to create a file called **forms.py** which houses the general
structure for any form we want in the application. **forms.py** should
be created in the base directory of the application. So for our program,
the path should look: **vetoffice/forms.py**.

Django forms are used with built-in *<a
href="https://docs.djangoproject.com/en/3.1/ref/class-based-views/generic-display/"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank" rel="noopener">generic classes</a>* to help build the
forms in the template. The code below will show a basic **forms.py**
setup:

```python
from django import forms
from .models import User
 
class TestForm(forms.ModelForm):
  class Meta:
    model = User
    fields = ("username")
```

The first thing that needs to be done in **forms.py** is that we need to
import `forms` from `django` and import any model we’ll be using from
`.models`. Then we can start constructing separate classes for each form
we want to build. In this example, we created a new class called
`TestForm`. `TestForm` takes in one parameter called `forms.ModelForm`
which is used to help build these forms in the template.

Inside of the `TestForm` class is `class Meta`. This inner `Meta` class
is used to let the application know what is inside of the parent class.
Notice that we have two properties in the `Meta` class:

-   `model` which tells the app what model we’ll be using
    -   In the example, we’re using the `User` model
-   `fields` which can be a tuple or list that informs the app what
    fields to use
    -   In the example, we’re using one field, `"username"`

If we wanted to include every field of a model, instead of writing it
all out inside of the `fields` list, we could include one string that
says `'__all__'` to indicate that we want every field to be used.



**1.**

In the previous exercises, we wrote in all the HTML for our forms. But
with generics, we don’t need to do that anymore. We’ve removed the code
from **owner_create_form.html** (that’s why the `owner/create` page is
empty) and we’ll start the process of using form generics.

Create **forms.py** inside of **vetoffice/**. Inside of **forms.py**,
import `forms` from `django` and `Owner` from `.models`.





**2.**

Create a class called `OwnerCreateForm` that takes `forms.ModelForm` as
a parameter.





**3.**

Add the `class Meta` to the `OwnerCreateForm` class.





**4.**

Inside of `Meta`, make sure the model is set to `Owner` and the accepts
the following fields: `"first_name"`, `"last_name"`, and `"phone"`. In a
few more exercises we’ll be able to view this form.





```python
from django import forms
from .models import Owner

class OwnerCreateForm(forms.ModelForm):
  class Meta:
    model = Owner
    fields = ("first_name", "last_name", "phone")
```

## Generics in Django: views.py

Now that we have the form made in **forms.py**, we can wire up our
**views.py** classes to render our templates. Remember we’ll need to
import both our form and our <a
href="https://docs.djangoproject.com/en/3.1/ref/class-based-views/generic-editing/"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank" rel="noopener">generic views</a>:

```python
from .forms import TestForm
from django.views.generic.edit import CreateView
```

Recall that we had to create a class for `TestForm` in **views.py**.
This class is usually named after the form, followed by the type of view
being created. For instance, with our `TestForm`, we would make a new
class that’s called `TestFormCreate` that takes in `CreateView`. A
sample of this class is below.

```python
class TestFormCreate(CreateView):
  model = TestModel
  template_name = "appName/form_template.html"
  form_class = TestForm
```

This class has three properties as seen above, those being the `model`,
the `template_name`, and the `form_class`. The `model` is assigned the
model we want to use. The `template_name` is the template file that we
want the form to be used in. And the `form_class` is going to be the
class that we created in **forms.py**. The `form_class` will also tell
Django to use this form within the template when building the form for
us.



**1.**

Remember that we need to tell **views.py** what we are going to be
using, which means that we need to add imports for:

-   the generic view, `CreateView` from `django.views.generic.edit`
-   the form that we just made: `OwnerCreateForm` from `.forms`





**2.**

Create the `OwnerCreate` class.





**3.**

Now that we have a place to put our creation form, let’s add everything
we need to the `OwnerCreate` class by:

-   Having the `model` set as `Owner`.
-   Having the `template_name` set as
    `"vetoffice/owner_create_form.html"`.
-   Having the `form_class` set as `OwnerCreateForm`.

**Note**: the `owner/create` page is still blank, but we’re really close
to rendering the form!





```python
from django.shortcuts import render
from django.views.generic import ListView
from .models import Owner
# Add your imports below:
from .forms import OwnerCreateForm
from django.views.generic.edit import CreateView

def home(request):
   context = {"name": "Djangover"}
   return render(request, "vetoffice/home.html", context)

class OwnerList(ListView):
   model = Owner

# Add your class below:
class OwnerCreate(CreateView):
  model = Owner
  template_name = "vetoffice/owner_create_form.html"
  form_class = OwnerCreateForm
```

## Generics in Django: Paths & Templates

Once the class is created in **views.py**, a path needs to be added to
**urls.py** so that the template can be rendered. The following `path()`
syntax should look familiar:

```python
path("path/name", views.TestFormCreate.as_view(), name="testformcreate"),
```

Now we can actually create the template that will house the form. This
template will just be a normal template and will be stored with all the
other templates. The file path should look like this:

```
appname/
├─ manage.py
└─ mysite/
    └─ templates
        └─ mysite/
            └─ form_template.html
```

This template will be treated as a normal template, meaning that it will
usually extend from **base.html** and include blocks. Inside of the
content blocks will be the following code.

```html
{% extends "appname/base.html" %}
 
{% block content %}
<form method="POST">
  {% csrf_token %}
  {{ form.as_p }}
  <input type="submit" value="Submit"/>
</form>
{% endblock %}
```

This code looks very similar to a normal HTML form, including the `form`
element with the `method` being `"POST"`, a `csrf_token`, and an
`<input>` element of type `"submit"`. However, the entirety of the form
is inside of the variable tag,
<a href="https://docs.djangoproject.com/en/3.1/ref/forms/api/#as-p"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank" rel="noopener">using <code
class="code__2rdF32qjRVp7mMVBHuPwDS">form.as_p</code></a>. Conveniently,
`form.as_p` tells the DTL to render all of the fields we included as
form inputs neatly inside `<p>` elements.



**1.**

The `owner/create` page still isn’t rendering correctly, so let’s start
to change that.

Inside of **urls.py**, add a path to `"owner/create"` with the view
`OwnerCreate.as_view()`. Set the name to `"ownercreate"`.





**2.**

Let’s set up our template now:

-   Create a template in **templates/vetoffice/** called
    **owner_create_form.html**.
-   Inside of this template, have it extend from
    **vetoffice/base.html**.
-   Add a block named `content`. Make sure to end the block as well.





**3.**

Inside of the content block, add the elements necessary to build the
HTML form using Django, including:

-   The `<form>`.
-   The `{% csrf_token %}`
-   The `<input>` of type `"submit"`.





**4.**

Notice our form is starting to take shape, let’s add in the rest.

We need to add `{{ form.as_p }}` inside the `<form>`.

Then run your code to see the finished form rendered in the
mini-browser! If you try submitting something, you’ll get an error about
redirecting — we’ll fix that in the next exercise.







```python
from django.urls import path

from . import views

# Add your path inside urlpatterns:
urlpatterns = [
   path("", views.home, name="home"),
   path("owner/list", views.OwnerList.as_view(), name="ownerlist"),
   path("owner/create", views.OwnerCreate.as_view(), name="ownercreate"),
]
```

## Redirecting

After a user submits their data, they should be redirected to another
page. Otherwise, the user might resubmit data again and create
duplicates. The Django convention is to create a <a
href="https://docs.djangoproject.com/en/3.1/ref/models/instances/#get-absolute-url"
class="e14vpv2g1 gamut-xro1w8-ResetElement-Anchor-AnchorBase e1bhhzie0"
target="_blank" rel="noopener"><code
class="code__2rdF32qjRVp7mMVBHuPwDS">.get_absolute_url()</code>
method</a>.

The `.get_absolute_url()` method goes inside of **models.py** and inside
of the class of the model that the form is using. For instance, if we
had used a model called `TestModel` in our forms, the `TestModel` class
would look like this in **models.py**:

```python
class TestModel(models.Model):
  field1 = models.CharField()
  field2 = models.CharField()
 
  def get_absolute_url(self):
    return "list"
```

The method `get_absolute_url()` has one parameter, `self`, and the
method is used to direct users to a specific path. Notice that we have
the method returning a string, which is the relative path name. This
string tells Django where to redirect our users to after submitting
their form. In the case described above, the users will be redirected to
the `"model/list"` path even though we’re only returning `"list"` —
that’s because Django is configured to assume we want to send users
somewhere related to the model.

By adding one method, Django lowers the chance of our users
re-submitting a form, or wondering if their information got sent!



**1.**

Inside of **models.py**, locate the `Owner` model. Then add the
`.get_absolute_url()` method and have it return `"list"`

After you’re done, try out the form!







```python
from django.db import models

class Owner(models.Model):
  first_name = models.CharField(max_length=30)
  last_name = models.CharField(max_length=30)
  phone = models.CharField(max_length=30)
  # Add your code below:
  def get_absolute_url(self):
    return "list"


class Patient(models.Model):
  DOG = "DO"
  CAT = "CA"
  BIRD = "BI"
  REPTILE = "RE"
  OTHER = "OT"
  ANIMAL_TYPE_CHOICES = [
    (DOG, "Dog"),
    (CAT, "Cat"),
    (BIRD, "Bird"),
    (REPTILE, "Reptile"),
    (OTHER, "Other"),
  ]
  animal_type = models.CharField(max_length=2, choices=ANIMAL_TYPE_CHOICES, default=OTHER)
  breed = models.CharField(max_length=200)
  pet_name = models.CharField(max_length=30)
  age = models.IntegerField(default=0)
  owner = models.ForeignKey(Owner, on_delete=models.CASCADE)
```

## Creating Additional Forms

When creating more forms for the Django application, they should all be
included inside of **forms.py**. For that reason, we need to make sure
that **forms.py** does not become too disorganized. We recommend keeping
as much relative data together and as close as possible. Try to keep the
code as clean as possible when writing a new form. This can be done by
keeping all information as close together as possible and commenting on
the code as you write it. Also, try not to add anything that isn’t
necessary.

With the methods used in this lesson, **forms.py** should not become too
large to handle. Even though larger application might have larger
**forms.py** the overall length should not have an impact on application
performance.



**1.**

We did some setup in **models.py**, **views.py**, **urls.py**, and
created both **vetoffice/templates/patient_list.html** and
**vetoffice/templates/patient_create_form.html**. But, the
`patient/create` page doesn’t load! That’s because **forms.py** still
needs come configuration.

Import another model called `Patient` into **forms.py**





**2.**

Now you can add a new form called `PatientCreateForm`. This form should
use the model `Patient` and have the fields: `"pet_name"`,
`"animal_type"`, `"breed"`, `"age"`, and `"owner"`.

Click on the “Add Patient” button to see your new form!







```python
from django import forms
# Import Patient below:
from .models import Owner, Patient

class OwnerCreateForm(forms.ModelForm):
  class Meta:
    model = Owner
    fields = ("first_name", "last_name", "phone")

# Add your class below:
class PatientCreateForm(forms.ModelForm):
  class Meta:
    model = Patient
    fields = ("animal_type", "breed", "pet_name", "age", "owner")
```

## Review

Congrats! That’s everything you need to know to build a basic form using
Django! Let’s go back over some of the important points from this
lesson.

-   Remember that in any application, forms are necessary for gathering
    data from the user.
-   These forms can easily be created in Django by using generics
    created in **forms.py**.
-   Forms are susceptible to attacks from malicious users, so make sure
    to add security such as a `{% csrf_token %}` and form validation.
-   Data from forms is submitted to `"POST"`, except for when using
    generics. When using generics, the data is submitted directly to the
    model and no extra work needs to be done.
-   **forms.py** can get rather large when working on some applications.
    While a large **forms.py** shouldn’t impact performance, it is
    important to try and keep **forms.py** as organized as possible.

You can see how forms are really important to the overall experience of
a Django app. Take this new knowledge and try applying it for your own
ideas!



Great job working through forms! If you want to challenge yourself
further, consider:

-   Creating forms to update and delete `Owner` instances
-   Creating forms to update and delete `Patient` instances
-   Link up these new forms inside their respective `ListView`s.


# Tourist Attractions with Forms

A local travel agency can’t keep up with all the new attractions being
added all over the country! They want an easier way to add not only new
attractions, but new states that they forgot to include originally. This
is keeping the agency from staying up to date on what attractions are in
each state and they need your help to create a solution to this!

Using the skills learned for Django on creating forms, we’ll practice:

-   Generic form creation
-   Using forms to create instances
-   Form security

Let’s get started!



Mark the tasks as complete by checking them off

## Working with Forms


1\.

After taking a look around we’ll see that this application looks a lot
like the original application we built before. The templates are about
the same and all we changed was what was inside of **models.py**.

Feel free to take a look at **models.py** and see what changes were
made. You’ll notice that some fields have a `verbose_name` argument.
This just changes how the field is displayed in a generic form. Look
over the new models and their fields.


2\.

Now we want to make it to where users can add the data themselves to
**models.py**. We’ll do this using Django generics.

To start we need to:

-   Create **forms.py**
-   Import `forms` from `django`
-   Import the `State` and `Attraction` models from `.models`




3\.

Now that we have imported the models, we can create the classes needed
for later use when submitting data to the forms and creating the forms.

To get started, create one class called `StateCreateForm`. Remember,
this class should inherit from `forms.ModelForm`.




4\.

Inside of our `StateCreateForm` class, we need to add in more
information.

Create a nested `Meta` class that contains a `model` property assigned
to `State` and `fields` assigned to `"__all__"` to display all of
`State`‘s fields.




5\.

Now that we have our `StateCreateForm` created, we’re going to want to
do the same thing again for a class called `AttractionCreateForm` for
`Attraction`.



## Moving on to Views


6\.

Once **forms.py** has been built, we can start connecting that to the
front end of our application. This will let Django render the form onto
a template.

To do this, we need to first navigate to **views.py**. Then:

-   import over `StateCreateForm` and `AttractionCreateForm` from
    `.forms`
-   import `CreateView`




7\.

Now that we imported what we need, we can start building the classes we
need to link to a template.

Go ahead and create the first class, `StateCreate()` which will need
`CreateView` as a parameter.




8\.

The `StateCreate` class will have three properties that set what goes
into the form.

The three properties are:

-   `model` set as `State`
-   `form_class` set as `StateCreateForm`
-   `template_name` set as `""`

You’ll change the value for `template_name` later!




9\.

Now that we have `StateCreate` complete, we can start working on the
`AttractionCreate`. Go ahead and create the `AttractionCreate` just like
the `StateCreate`. Make sure to include the `CreateView` parameter and
to include all the same 3 properties.



## Modifying URLs


10\.

Now that we have our views created, we can add our `path()`s to our
**urls.py** that use those views.

Start by navigating to **urls.py** and adding a `path()` leading to
`"state/create"`. This path should use the
`views.StateCreate.as_view()`. Add an appropriate name so it can be
referenced later, like `"statecreate"`.




11\.

Once the path is set up to create a `State`, we can do the same thing
for an `Attraction`. Create a path that uses `"attraction/create"` along
with the right view and give it a name of `"attractioncreate"`.

## Adding Our Templates


12\.

Since most of the back-end work is done, we can create our templates
inside of **templates/tourist_attractions/**. This is where we’ll make
everything we want the user to see and will house our forms. Both of
these templates will be the same, so repeat these instructions for the
second template.

Go ahead and create a template for `State` name the template
`state_create_form.html`. Inside of this template, we’ll need to:

-   Extend the template from `"tourist_attractions/base.html"`.
-   Load in `static`
-   Add a head block that will add in the same CSS file as in
    **home.html**.
-   Finally, go ahead and create the content block for the template.




13\.

Inside of your content block, add a `<h1>` signifying whether users are
creating a new state or new attraction.

Then add a `<form>` element that uses a `csrf_token` and loads in the
`form.as_p` variable. Finally, add a submit button and close the
`<form>` element.




14\.

Once our template for `State` is created, we can move on to creating our
`Attraction` template.

Create a new template for the `Attraction` model. This time name the
file, `attraction_create_form.html`.

Once that’s created, go ahead and copy and paste everything from our
`State` template to our `Attraction` template. Remember to change the
`<h1>` text to now mention `Attraction`, but just like that we’ve
created forms for our `State` and `Attraction` model!




15\.

Now that the templates are created, we can go back to our **views.py**
and change the empty strings for both `template_name` fields to their
correlating templates.

It also means that we will finally be able to render the template at the
defined path! Remember the paths are:

```python
# urls.py
path("state/create", views.StateCreate.as_view(), name="statecreate")
path("attraction/create", views.AttractionCreate.as_view(), name="attractioncreate")
```

We can find the respective templates at
`https://localhost/tourist_attractions/state/create` and
`https://localhost/tourist_attractions/attraction/create`!



## Adding a Redirect


16\.

With the form now rendering properly, we want to make sure that when the
user submits the data they are redirected to the homepage.

To do this, we need to add a `get_absolute_url()` method to both the
`State` and `Attraction` models in **models.py**. Have the method return
to the home page (`"/tourist_attractions/"`) in both cases.



## Linking to the Forms


17\.

While our forms have been created, the users don’t have a way to find
them easily. But we want our users to be able to find them easily.

To do this, we’re going to navigate to **home.html** and:

-   Under the closing `</table>` tag, add a link to our `State` template
-   Set the `href` set to `"{% url 'statecreate' %}"`
-   Have the text read `Add a state`




18\.

Now we can create another link to the `AttractionCreate` path.




19\.

And that’s it, congrats! We’ve now created two forms for adding any
states or attractions. Try out your forms, first create a state, then
create an attraction. Watch your home page populate!

If you want, try adding some more fields to the models in **models.py**
that you think would be useful and add those to the forms as well! One
field you could add would be to add the city to the `Attraction` model.
You can also add in other forms for updating and deleting instances as
well!



[Django Project Tourist Attractions with Forms](https://www.youtube.com/watch?v=z96peq-ceG4)

```bash
#!/bin/bash

red=`tput setaf 1`
green=`tput setaf 2`
reset=`tput sgr0`

project_name='touristAttractions'
echo "${green}>>> The name of the project is '$PROJECT'.${reset}"
app_name='tourist_attractions'
templates_path="$app_name"\/templates\/"$app_name"
echo "${green}>>> Remove project directory if exists${reset}"
rm -rf $project_name
rm -rf env


echo "${green}>>> Creating virtualenv${reset}"
echo "${green}>>> venv is created${reset}"
python3 -m venv env
echo "${green}>>> activate the venv${reset}"
source env/bin/activate
echo "${green}>>> upgrading pip version${reset}"
pip install -U  --upgrade pip
echo "${green}>>> Installing the Django${reset}"
pip install django
echo "${green}>>> Creating the project '$project_name' ...${reset}"
django-admin startproject $project_name && cd $project_name
echo "${green}>>> Creating the app '$app_name' ...${reset}"
python manage.py startapp $app_name
echo "${green}>>> Adding the app '$app_name' to INSTALLED_APP ...${reset}"
sed -i '' "s,INSTALLED_APPS = \[,INSTALLED_APPS = \[\n    \'$app_name\'\,,g"  $project_name/settings.py

echo "${green}>>> Creating forms.py${reset}"
cat << 'EOF' > $app_name/forms.py
from django import forms
from .models import State, Attraction

class StateCreateForm(forms.ModelForm):
  class Meta:
    model = State
    fields = '__all__'

class AttractionCreateForm(forms.ModelForm):
  class Meta:
    model = Attraction
    fields = '__all__'
EOF

echo "${green}>>> Editing models.py${reset}"
cat << 'EOF' > $app_name/models.py
from django.db import models

class State(models.Model):
  stateName = models.CharField(max_length=50, verbose_name="State Name")
  stateAbbreviation = models.CharField(max_length=3, verbose_name="State Abbreviation")

  def __str__(self):
    return '{}'.format(self.stateName)

  def get_absolute_url(self):
    return '/tourist_attractions/'

class Attraction(models.Model):
  homeState = models.ForeignKey(State, on_delete=models.CASCADE, verbose_name="Home State")
  attractionName = models.CharField(max_length=200, verbose_name="Attraction Name")

  def __str__(self):
    return '{}'.format(self.attractionName)

  def get_absolute_url(self):
    return '/tourist_attractions/'
EOF

echo "${green}>>> Editing app urls.py${reset}"
cat << 'EOF' > $app_name/urls.py
from django.urls import path

from . import views

urlpatterns = [
  path("", views.home, name="home"),
  path("details/<statename>", views.details, name="details"),
  path('state/create', views.StateCreate.as_view(), name='statecreate'),
  path('attraction/create', views.AttractionCreate.as_view(), name='attractioncreate'),
]
EOF
echo "${green}>>> Editing project urls.py${reset}"
sed -i ''  "s,from django.urls import,from django.urls import include\,,g; s,urlpatterns = \[,urlpatterns = \[\n    path\(\'tourist_attractions\/\'\, include\(\'$app_name\.urls\'\)\)\,,g" $project_name/urls.py

echo "${green}>>> Editing views.py${reset}"
cat << 'EOF' > $app_name/views.py
from django.shortcuts import render, get_object_or_404
from .models import State, Attraction
from .forms import StateCreateForm, AttractionCreateForm
from django.views.generic.edit import CreateView

def home(request):
  all_attractions = Attraction.objects.all()
  context = {"attractions" : all_attractions}
  return render(request, 'tourist_attractions/home.html', context)

def details(request, statename):
  attractions = Attraction.objects.all()
  context = {"attractions" : attractions, "statename" : statename.replace("-", " ")}
  return render(request, 'tourist_attractions/details.html', context)

class StateCreate(CreateView):
  model = State
  form_class = StateCreateForm
  template_name = 'tourist_attractions/state_create_form.html'

class AttractionCreate(CreateView):
  model = Attraction
  form_class = AttractionCreateForm
  template_name = 'tourist_attractions/attraction_create_form.html'  
EOF

echo "${green}>>> Creating templates${reset}"
mkdir -p $templates_path

echo "${green}>>> Editing templates${reset}"
echo "${green}>>> Creating base.html${reset}"
cat << 'EOF' > $templates_path/base.html
<!DOCTYPE html>

<head>
  {% block head %}
  {% endblock %}
</head>

<body>
  <a href="{% url 'home' %}"><h2>Take me home</h2></a>
  {% block content %}
  {% endblock %}
</body>
EOF

echo "${green}>>> Creating home.html${reset}"
cat << 'EOF' > $templates_path/home.html
{% extends 'tourist_attractions/base.html' %}
{% load static %}

{% block head %}
<link rel="stylesheet" href="{% static 'tourist_attractions/style.css' %}">
{% endblock %}

{% block content %}
<h1>This is a list of some attractions in America!</h1>

<table>
  <tr>
    <th>Attraction</th>
    <th>State</th>
    <th>State Details</th>
  </tr>
  {% for item in attractions|dictsort:'homeState.stateName' %}
  <tr>
    <td>{{ item.attractionName }}</td>
    <td>{{ item.homeState }}</td>
    <td><a href="{% url 'details' item.homeState|slugify %}">State Details</a></td>
    </tr>
    {% endfor %}
</table>
<a href="{% url 'statecreate' %}">Add a state</a>
<br>
<a href="{% url 'attractioncreate' %}">Add an attraction</a>
{% endblock %}
EOF

echo "${green}>>> Creating details.html${reset}"
cat << 'EOF' > $templates_path/details.html
{% extends 'tourist_attractions/base.html' %}
{% load static %}

{% block head %}
<link rel="stylesheet" href="{% static 'tourist_attractions/style.css' %}">
{% endblock %}

{% block content %}
<h1>This is a list of tourist attractions for {{ statename|title }}!</h1>

<table>
    <tr>
        <th>Attraction</th>
        <th>State</th>
    </tr>
    {% for item in attractions|dictsort:'homeState' %}
    {% if item.homeState|lower == statename %}
    <tr>
        <td>{{ item.attractionName }}</td>
        <td>{{ item.homeState }}</td>
    </tr>
    {% endif %}
    {% endfor %}
</table>
{% endblock %}
EOF

echo "${green}>>> Creating state_create_form.html${reset}"
cat << 'EOF' > $templates_path/state_create_form.html
{% extends 'tourist_attractions/base.html' %}

{% load static %}

{% block head %}
<link rel="stylesheet" href="{% static 'tourist_attractions/style.css' %}">
{% endblock %}

{% block content %}
<h1>
  Add a new State
</h1>
<form method="POST" action="">
  {% csrf_token %}
  {{ form.as_p }}
  <input type="submit" value="Submit"/>
</form>
{% endblock %}
EOF

echo "${green}>>> Creating attraction_create_form.html${reset}"
cat << 'EOF' > $templates_path/attraction_create_form.html
{% extends 'tourist_attractions/base.html' %}

{% load static %}

{% block head %}
<link rel="stylesheet" href="{% static 'tourist_attractions/style.css' %}">
{% endblock %}

{% block content %}
<h1>
  Add a new Attraction
</h1>
<form method="POST" action="">
  {% csrf_token %}
  {{ form.as_p }}
  <input type="submit" value="Submit"/>
</form>
{% endblock %}
EOF

echo "${green}>>> Creating static directory${reset}"
mkdir -p $app_name/static/$app_name

echo "${green}>>> Creating style.css${reset}"
cat << 'EOF' > $app_name/static/$app_name/style.css
table, th, td {
 border: 1px solid black;
}
table {
 border-collapse: collapse;
 width: 100%;
}

tr:nth-child(even) {
  background-color: #eee;
}
tr:nth-child(odd) {
  background-color: #fff;
}

body {
  background-color: #e8f4f8;
  margin: 40px 20px 10px;
}
EOF

# List installed Python packages
pip freeze -l > requirements.txt
```