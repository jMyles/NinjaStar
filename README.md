# Ninja Star ✴️🌠✴️
A tool for handling bytes-on-the-wire to and from API Star, enabling easy creation of asynchronous and websocket-driven python web applications.

-------------------------------------------------------------------------------

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.  See [deployment](docs/deployment.md/) for notes on how to deploy the project on a live system.

#### Installation

```bash
git clone https://github.com/jMyles/NinjaStar.git
```

#### Prerequisites

Install the Ninja Star dependencies by running
```
pip install -r requirements.txt
```

#### Quick Start

Create a file to contain your application configuration - let's say `run.py`.


Provide the database configuration settings.
```py
settings = {
    "DATABASE": {
        "URL": "postgresql://:@localhost/apistar",
        "METADATA": Base.metadata
    }
}
```

Instantiate an App
```py
app = App(routes=routes, settings=settings, commands=[create_sqlalchemy_tables])

ninja_star = NinjaStar(wsgi_app=app)
ninja_star.run()

```

Finally, run the application:
```bash
python run.py
```

--------------------------------------------------------------------------------

## Built With

* [Twisted](https://github.com/twisted/twisted)


## Contributing

Please read [contributing.md](docs/contributing.md/) for details on our [code of conduct](docs/conduct.md/), and running the automated tests.


## Future

* throwing_star - a context manager for handling websocket and pubsub traffic


## Authors

* **Justin Myles Holmes**
* **Kieran Robert Prasch**


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE) file for details


## Acknowledgments

* Hendrix
* Twisted
* API Star
