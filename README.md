# HashThat

HashThat is a small Django app for generating SHA-256 hashes from text. It provides a form-based page that stores submitted text and its hash, plus a quick hash endpoint used by the homepage AJAX preview.

## Features

- Generate SHA-256 hashes from submitted text.
- Save hashed text in the database.
- View a saved hash and its original text.
- Preview a hash as you type via the `/quickhash` endpoint.

## Requirements

- Python 3
- pip

Python package dependencies are pinned in `requirements.txt`.

## Setup

From the repository root:

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
```

## Run the app

```bash
python manage.py runserver
```

Then open <http://localhost:8000/>.

## Usage

- Enter text on the homepage and submit the form to save and view its SHA-256 hash.
- Use `/quickhash?text=hello` to get a JSON response with the SHA-256 hash for `hello`.

## Tests

Run the Django test suite with:

```bash
python manage.py test
```

Some tests use Selenium with Firefox and require a compatible browser and driver.
