# Flask RESTful API Kickstart

This project template aims to help you kickstart your RestAPI project by giving you a better starting point.
Project template is based on Flask web framework with Flask-RESTful plugin, Flask-SQLAlchemy plugin for ORM and a SQLite DB.

## Installing 

You can install by source code.

Use `virtualenv` (pip install virtualenv):

    > git fork ...
    > cd ...
    > virtualenv --no-site-packages venv
    > source venv/bin/activate
    > python setup.py install
    > python setup.py test

## Usage


### create
    > curl -d "name=chair" -X POST http://127.0.0.1:5000/item
    {
        "id": 1,
        "uuid": "e5dfe582-a8b0-4154-bc39-7682bf5e0328",
        "name": "chair",
        "created": "2020-08-15 05:08:41.097580",
        "updated": "None"
    }
    
### select all

    > curl -d http://127.0.0.1:5000/items
    "items": [
        {
            "id": 1,
            "uuid": "e5dfe582-a8b0-4154-bc39-7682bf5e0328",
            "name": "chair",
            "created": "2020-08-15 05:08:41.097580",
            "updated": "2020-08-16 03:26:21.109505"
        }
    ]
}

### select

    > curl http://127.0.0.1:5000/item/e5dfe582-a8b0-4154-bc39-7682bf5e0328
    {
    "id": 2,
    "uuid": "e5dfe582-a8b0-4154-bc39-7682bf5e0328",
    "name": "http://log?.co.il",
    "created": "2020-08-15 05:08:41.097580",
    "updated": "2020-08-16 03:26:21.109505"
     }

### select all

    > curl -d http://127.0.0.1:5000/items
    "items": [
        {
            "id": 1,
            "uuid": "e5dfe582-a8b0-4154-bc39-7682bf5e0328",
            "name": "chair",
            "created": "2020-08-15 05:08:41.097580",
            "updated": "2020-08-16 03:26:21.109505"
        }
            ]
    }
### update

    > curl -d "name=table" -X PUT http://127.0.0.1:5000/item/e5dfe582-a8b0-4154-bc39-7682bf5e0328

    {
    "id": 2,
    "uuid": "e5dfe582-a8b0-4154-bc39-7682bf5e0328",
    "name": "table",
    "created": "2020-08-16 03:12:49.085620",
    "updated": "2020-08-16 05:02:53.773666"
     }


### delete

    > curl -X DELETE http://127.0.0.1:5000/item/e5dfe582-a8b0-4154-bc39-7682bf5e0328
    {
        "message": "item deleted >> {'id': 2, 'uuid': 'e5dfe582-a8b0-4154-bc39-7682bf5e0328', 'name': 'table', 'created': '2020-08-16 03:12:49.085620', 'updated': '2020-08-16 05:02:53.773666'}"
    }



