# ScoreCard Flask Project

Using Flask to build a Restful API Server for ScoreCard.

Integration with Flask-restplus, Flask-Cors, Flask-Testing, Flask-SQLalchemy,and Flask-OAuth extensions.

### Extension:
- Restful: [Flask-restplus](http://flask-restplus.readthedocs.io/en/stable/)

- SQL ORM: [Flask-SQLalchemy](http://flask-sqlalchemy.pocoo.org/2.1/)

- OAuth: [Flask-OAuth](https://pythonhosted.org/Flask-OAuth/) [Flask-Dance](https://flask-dance.readthedocs.io/en/latest/) 

## Installation

Install with pip:

```
$ pip install -r requirements.txt
```

## Flask Application Structure 
```
.
|──────app/
| |────app.yaml
| |────templates/
| | |────index.html
| | |────...html
| | |────...html
| |────static/
| |────models.py
| |────requirements.txt
| |────oauth.py
| |────credentials.json
| |────config.py
| |────cli.py
| |────app.py
|──────venv/


change app.py to main.py to run in production for google cloud
```

## Flask Configuration

#### Example

```
app = Flask(__name__)
app.config['DEBUG'] = True
```
### Configuring From Files

#### Example Usage

```
app = Flask(__name__ )
app.config.from_pyfile('config.Development.cfg')
```

#### Builtin Configuration Values


JSON_SORT_KEYS : By default Flask will serialize JSON objects in a way that the keys are ordered.

- [reference¶](http://flask.pocoo.org/docs/0.12/config/)


### OAuth Setup
credintials.json has keys

 
## Run Flask
### Run flask for develop
```
$ cd TAIV_Score
$ source venv/bin/activate
$ cd app
$ flask run
```
In flask, Default port is `5000`

Scorecard default page:  `http://127.0.0.1:5000/`

### Run flask for production

** Run with gunicorn **

In  app/

```
$ gunicorn -w 4 -b 127.0.0.1:5000 run:app

```

* -w : number of worker
* -b : Socket to bind

## Reference

Offical Website

- [Flask](http://flask.pocoo.org/)
- [Flask restplus](http://flask-restplus.readthedocs.io/en/stable/)
- [Flask-SQLalchemy](http://flask-sqlalchemy.pocoo.org/2.1/)
- [Flask-OAuth](https://pythonhosted.org/Flask-OAuth/)
- [gunicorn](http://gunicorn.org/)

Tutorial

- [Flask Overview](https://www.slideshare.net/maxcnunes1/flask-python-16299282)
- [In Flask we trust](http://igordavydenko.com/talks/ua-pycon-2012.pdf)
