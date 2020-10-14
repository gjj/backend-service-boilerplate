# backend-service-boilerplate

This repository contains boilerplate codes to build an API service using Python Flask.

## Example

A sample endpoint for Calculate Square is in this repo, where you can `POST` to the API endpoint `/square` with the input:

```json
{ "input": 5 }
```

You can explore the `/square` endpoint too:

- Go to `square.py` under `app/routes` folder and you will find a `POST` method with route `/square`
- Write your implementation in this method
- Note the `__init__.py` file in each folder, this file makes Python treat directories containing it to be loaded in a module (you can refer to [this guide](https://chrisyeh96.github.io/2017/08/08/definitive-guide-python-imports.html#basic-definitions) for more details)

## To run

It is highly recommended for you to use a `virtualenv`, so that you can keep your `requirements.txt` small by having only the packages you need.

Below are instructions for installing `virtualenv` specific to Windows. For Mac OS, coming soon. ™️

```sh
pip install virtualenv
```

Next up, create the virtual environment. This will create a `venv` folder that will be ignored by Git.

```sh
python -m venv venv
```

You need to run the virtual environment and install the required packages from within `venv`.

```sh
.\venv\Scripts\activate
pip install -r requirements.txt
```

Finally, you may now run the services!

```sh
python app.py
```

If you add on more packages, remember to run the following command to update `requirements.txt`:

```sh
pip freeze > requirements.txt
```

## Test

To run all unit tests, simply run the following command:

```sh
pytest
```

## CI/CD

In the `.circleci` folder, it contains an example `config.yml` file that has two important stages:

- `install` stage to install all required packages
- `test` stage to run all unit tests

## Deployment to AWS

This boilerplate repository also contains a `Procfile`, which means you can setup this way:

- Use AWS CodePipeline with this repository
- Deploy to AWS Elastic Beanstalk using the Python option

## Docker

Still tinkering with it for now.
