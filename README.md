# Joplin Api

The API of [Joplin Editor](https://joplin.cozic.net/) in Python 3.6+

## requirements

* python 3.6+
* [requests](http://docs.python-requests.org/)

## Installation 

```
git clone  https://github.com/foxmask/joplin-api
pip install requests
```

## Using Joplin API

```
>>> from joplin_api import JoplinApi
>>> joplin = JoplinApi('Api', token='the token provided by Joplin in the WebClipper menu:P'))
>>> joplin.ping()  # to check if the service is up
>>> joplin.get_folders() # to get all the folders
>>> folder_title = 'Default'
>>> folder = joplin.create_folder(folder_title) # to create a folder
>>> # to create a new note
>>> note_title = 'My title'
>>> note_body = '# My Title ## My Subtitle my body'
>>> joplin.create_note(note_title, note_body, folder['id'])
>>> joplin.get_notes() # to get all the notes
>>> joplin.get_tags() # to get all the tags
>>> joplin.version() # to get the version of joplin
```
