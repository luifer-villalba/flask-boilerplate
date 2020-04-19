# Flask Server Boilerplate

A minimal ready-to-go Flask Server with minimal structure.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

## Features
- User authentication
    - JWT
    - Blacklist token on user logout
- Structure Skeleton
    - Controller
    - Model
    - Service
    - DTO
    - Decorator
- Unit Tests
- Database Configuration
    - Default SQLite configuration
    - Postgres database configuration as a second option
- Issues and Pull Requests templates

### Prerequisites

For this project, is recommended to have `Python3` installed.

### Run

Activate local environment
```
source env/bin/activate 
```

Or, if you want to use your own interpreter get the dependencies using this command
```
pip install -r requirements.txt
```

Database Initialization
```
python managepy db init
```

Create a migration script from the detected changes in the model using the `migrate` command. This doesn't affect the database yet.
```
python manage.py db migrate --message 'initial database migration'
```

Apply the migration script to the database by using the `upgrade` command
```
python manage.py db upgrade
```

Run your server
```
python manage.py run
```

Open the following url on your browser to view swagger documentation
```
http://127.0.0.1:5000/
```

### Using Postman
Authorization header is in the following format:
```
Key: Authorization
Value: "token_generated_during_login"
```

## Running the tests

To run tests use the following command
```
python manage.py test
```

Also, it's a good test for your local environment to check if is everything OK and ready to go.

## TODO
- [ ] Prerequisite details
- [ ] Tests details
- [ ] Deployment Steps
- [ ] Versioning details


## Built With

* [Flask](https://flask.palletsprojects.com/en/1.1.x/) - Python minimal framework

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Authors

* **Luifer Villalba** - [Github](https://github.com/luifer-villalba), [Resume](https://luifervillalba.com)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* freeCodeCamp [Tutorial](https://www.freecodecamp.org/news/structuring-a-flask-restplus-web-service-for-production-builds-c2ec676de563/)
