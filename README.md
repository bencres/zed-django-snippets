# Django Snippets for Zed
A collection of useful Django snippets for Zed.

## Models

| Prefix | Description |
| ------- | ------------ |
| `djmodel` | Defines a Django model with `created_at` and `updated_at` timestamps. |
| `djchar` | Adds a `CharField` to a model. |
| `djtext` | Adds a `TextField` to a model. |
| `djint` | Adds an `IntegerField` to a model. |
| `djdecimal` | Adds a `DecimalField` with `max_digits` and `decimal_places`. |
| `djbool` | Adds a `BooleanField` with a default value. |
| `djdate` | Adds a `DateField`, typically with `auto_now_add=True`. |
| `djdatetime` | Adds a `DateTimeField`, usually with `auto_now_add=True`. |
| `djemail` | Adds an `EmailField` for storing email addresses. |
| `djurl` | Adds a `URLField` for storing URLs. |
| `djslug` | Adds a `SlugField` with a unique constraint. |
| `djimage` | Adds an `ImageField` for image uploads. |
| `djfile` | Adds a `FileField` for general file uploads. |
| `djfk` | Defines a `ForeignKey` relationship with an on-delete behavior. |
| `djo2o` | Defines a `OneToOneField` relationship. |
| `djm2m` | Defines a `ManyToManyField` relationship. |
| `djjson` | Adds a `JSONField` to store structured JSON data. |
| `djmeta` | Adds a `Meta` class to customize model metadata. |
| `djstr` | Defines a model’s `__str__()` method for readable names. |
| `djgeturl` | Adds a `get_absolute_url()` method for model instances. |
| `djsave` | Adds a custom `save()` method with an override option. |
| `djmanager` | Creates a custom model manager with additional query methods. |
| `djqueryset` | Defines a custom `QuerySet` class for model filtering. |
| `djabstract` | Defines an abstract base model for inheritance. |
| `djproperty` | Adds a Python `@property` method to a model. |
| `djchoices` | Defines a text-based choice enumeration class. |

---

## Views (Class-Based)

| Prefix | Description |
| ------- | ------------ |
| `djlistview` | Defines a Django `ListView` for displaying lists of objects. |
| `djdetailview` | Defines a `DetailView` for showing single object details. |
| `djcreateview` | Defines a `CreateView` for creating new objects. |
| `djupdateview` | Defines an `UpdateView` for editing existing objects. |
| `djdeleteview` | Defines a `DeleteView` for deleting objects. |
| `djtemplateview` | Defines a `TemplateView` that renders a static template. |
| `djformview` | Defines a `FormView` for handling user-submitted forms. |
| `djgetcontext` | Overrides `get_context_data` to add custom context. |
| `djgetqueryset` | Overrides `get_queryset` to filter database queries. |
| `djformvalid` | Overrides `form_valid` to add logic before saving a form. |
| `djdispatch` | Overrides `dispatch` for pre-processing requests. |
| `djloginrequired` | Adds `LoginRequiredMixin` to restrict views to authenticated users. |
| `djpermission` | Adds `PermissionRequiredMixin` for permission-based access. |
| `djredirectview` | Defines a `RedirectView` to redirect users to a URL. |

---

## Views (Function-Based)

| Prefix | Description |
| ------- | ------------ |
| `djfbv` | Defines a standard function-based view. |
| `djfbvpost` | Defines a function-based view with POST handling logic. |
| `djrequirehttp` | Adds `@require_http_methods` decorator to restrict HTTP methods. |
| `djlogin` | Adds `@login_required` decorator for authentication protection. |
| `djperm` | Adds `@permission_required` decorator for permission checks. |

---

## URLs

| Prefix | Description |
| ------- | ------------ |
| `djpath` | Defines a standard URL pattern using `path()`. |
| `djpathpk` | Defines a URL pattern with an integer `pk` parameter. |
| `djpathslug` | Defines a URL pattern with a slug parameter. |
| `djrepath` | Defines a regex-based URL pattern using `re_path()`. |
| `djinclude` | Includes another app’s URL configuration. |
| `djurlpatterns` | Sets up a full `urlpatterns` list with boilerplate. |
| `djcrudurls` | Creates a full CRUD URL pattern set for a model. |
| `djapipath` | Defines an API endpoint URL pattern. |
| `djnamespace` | Includes URLs with a Django namespace. |

---

## Forms

| Prefix | Description |
| ------- | ------------ |
| `djmodelform` | Defines a `ModelForm` for a specific model. |
| `djmodelformwidgets` | Creates a `ModelForm` with customized widgets. |
| `djform` | Defines a basic Django form with one or more fields. |
| `djfchar` | Adds a `CharField` to a form. |
| `djfemail` | Adds an `EmailField` to a form. |
| `djfint` | Adds an `IntegerField` to a form. |
| `djfbool` | Adds a `BooleanField` to a form. |
| `djfchoice` | Adds a `ChoiceField` with predefined options. |
| `djfdate` | Adds a `DateField` with an HTML5 date input widget. |
| `djffile` | Adds a `FileField` to handle file uploads. |
| `djfimage` | Adds an `ImageField` to handle image uploads. |
| `djfmodelchoice` | Adds a `ModelChoiceField` linked to a model’s queryset. |
| `djfmodelmultiple` | Adds a `ModelMultipleChoiceField` linked to a queryset. |
| `djclean` | Defines a `clean_<field>()` method for field-level validation. |
| `djcleanall` | Defines a `clean()` method for cross-field validation. |
| `djforminit` | Overrides form `__init__` for custom initialization. |
| `djformsave` | Overrides `save()` method for ModelForm customization. |
| `djformset` | Creates a `modelformset_factory` for multiple objects. |
| `djinlineformset` | Creates an `inlineformset_factory` for parent-child models. |

---

## Template Tags

For the template tags to be suggested, you need to have the [Django extension](https://github.com/joshuadavidthomas/zed-django) installed.

Currently, we're using the template tags available in Django 5.2, so the syntax may vary depending on your Django version.

If they're still not appearing after installing the extension, add the following to your zed's `settings.json` file (or refer to their docs for more info):

```
{
  "file_types": {
    "Django": ["**/templates/**/*.html"]
  }
}
```

| Prefix | Description |
| ------- | ------------ |
| `autoescape` | Controls the current auto-escaping behavior. |
| `block` | Adds a block with a name. |
| `comment` | Ignores everything between the tags. |
| `csrf_token` | Inserts CSRF token for forms. |
| `cycle` | Cycles among values in a loop. |
| `debug` | Outputs debugging information. |
| `extends` | Extends a parent template. |
| `filter` | Filters the contents through one or more filters. |
| `firstof` | Outputs the first variable that is not False. |
| `for` | Loops over each item in an array. |
| `for_empty` | For loop with empty clause. |
| `if` | Evaluates a variable and outputs content if true. |
| `if_else` | If statement with else clause. |
| `if_elif_else` | If statement with elif and else clauses. |
| `ifchanged` | Checks if a value has changed from the last iteration. |
| `include` | Loads a template and renders it with the current context. |
| `include_with` | Includes a template with additional context. |
| `load` | Loads a custom template tag library. |
| `lorem` | Displays random lorem ipsum text. |
| `now` | Displays the current date and/or time. |
| `regroup` | Regroups a list by a common attribute. |
| `resetcycle` | Resets a previous cycle. |
| `spaceless` | Removes whitespace between HTML tags. |
| `static` | Links to static files. |
| `templatetag` | Outputs template syntax characters. |
| `url` | Returns an absolute path reference. |
| `verbatim` | Stops the template engine from rendering the contents. |
| `widthratio` | Calculates ratio of a value to a maximum value. |
| `with` | Caches a complex variable under a simpler name. |
