# django-libelektra

This repository is my homework for the university lecture "194.030 Configuration Management" at TU Wien.

## Specification (HW1)

An elektra-specification for the most important Django settings can be found in `spec/django.spec.ni`:

* `ALLOWED_HOSTS`
* `CSRF_TRUSTED_ORIGINS`
* `DATABASE`: `Dict`
  * Key-Value-Pair.
  * Value is another `Dict`:
    * `ENGINE`
    * `NAME`
    * `USER`
    * `PASSWORD`
    * `HOST`
    * `PORT`
* `DEBUG`
* `INSTALLED_APPS`

Django's license can be found [here](https://github.com/django/django/blob/main/LICENSE).

Specification for Django's settings can be found [here](https://docs.djangoproject.com/en/4.0/ref/settings/).

## Sample Application (HW2)

### Installation

Since this is a very generic python project, installation is very easy:

1. Checkout source code

   ```sh
   git clone ...
   ```

2. Create a new [virtual environment](https://docs.python.org/3/library/venv.html) named `venv` with system site packages:

   ```sh
   python3 -m venv venv --system-site-packages
   ```

3. Install requirements:

   ```sh
   ./venv/bin/pip install -r requirements.txt
   ```

### Running

1. Mount specification and apply test data:

   ```sh
   ./spec/test-spec.sh
   ```

2. initialize db and apply migrations:

   ```sh
   ./venv/bin/python3 manage.py migrate
   ```

3. Run server:

   ```sh
   ./venv/bin/python3 manage.py runserver
   ```

### Testing

Open <http://127.0.0.1:8000> in your browser.
