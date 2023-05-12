---
title: Coding with Environment Variables
layout: page
parent: Coding
---

# Coding with Environment Variables

Dotenv is a simple and effective tool for managing environment variables in Python. It's often used in development environments to store configuration settings, especially sensitive information like API keys and database credentials.

## Contents

1. [Installation](#installation)
2. [Creating and Using a .env File](#creating-and-using-a-.env-file)
3. [Environment Variables in Python](#environment-variables-in-python)
4. [Sensitive Information and Environment Variables](#sensitive-information-and-environment-variables)
5. [Setting Environment Variables in Linux and Windows](#setting-environment-variables-in-linux-and-windows)
6. [Setting Environment Variables in Cloud Services](#setting-environment-variables-in-cloud-services)

## Installation <a name="installation"></a>

Dotenv can be installed via pip, Python's package installer. Simply open your terminal and execute the following command:

```bash
pip install python-dotenv
```

Ensure that pip is correctly installed and updated in your environment before running the command.

## Creating and Using a .env File <a name="creating-and-using-a-.env-file"></a>

A .env file is a simple text file that contains key-value pairs. Each line in the file represents an environment variable.

For example:

```
DATABASE_URL=postgresql://localhost/mydatabase
SECRET_KEY=my-secret-key
```

To use these environment variables in your Python application, you need to load them. You can do this automatically when your application starts using the `load_dotenv` function from the dotenv module.

Here's an example:

```python
from dotenv import load_dotenv

load_dotenv()  # take environment variables from .env.
```

This will take environment variables from a .env file that's in the same directory as the Python script that's running and add them to the environment variables that are available to your script.

## Environment Variables in Python <a name="environment-variables-in-python"></a>

Once you've loaded environment variables using `load_dotenv`, you can access them in your Python scripts through the `os.environ` object, which is a dictionary-like object.

For example:

```python
import os

database_url = os.environ['DATABASE_URL']
secret_key = os.environ['SECRET_KEY']
```

## Sensitive Information and Environment Variables <a name="sensitive-information-and-environment-variables"></a>

Environment variables are a secure way to manage sensitive data, such as API keys, database passwords, and other credentials. This data is only available to the process where the variable is set and is cleared when the process ends.

Furthermore, by using a .env file, you can avoid hardcoding sensitive data directly into your application code. This is especially useful when working on open source projects, as it prevents sensitive data from being accidentally committed and pushed to public code repositories.

Remember to add your .env file to your `.gitignore` file to ensure it doesn't get committed to your Git repository.

## Setting Environment Variables in Linux and Windows <a name="setting-environment-variables-in-linux-and-windows"></a>

### Linux

In Linux, you can set environment variables in the shell using the `export` command:

```bash
export DATABASE_URL=postgresql://localhost/mydatabase
```

### Windows

In Windows, use the `setx` command in the Command Prompt:

```cmd
setx DATABASE_URL "postgresql://localhost/mydatabase"
```

## Setting Environment Variables in Cloud Services <a name="setting-environment-variables-in-cloud-services"></a>

### Azure Functions and App Service

In Azure Functions and Azure App Service, environment variables are called Application Settings. You can set them in the Azure portal, under the "Settings" section of your App Service or Function App.

### AWS Lambda

In AWS Lambda, environment variables can be set in the AWS Management Console. In the function configuration section, there's an "Environment variables" section where you can set key-value pairs.

### Docker

For Docker, you can use the `-e` flag when running your container to set environment variables:

```bash
docker run -e "DATABASE_URL=postgresql://localhost/mydatabase" -e "SECRET_KEY=my-secret-key" my-python-app
```

Alternatively, you can use an `env_file` in your `docker-compose.yml`:

```yaml
version: '3'
services:
  web:
    build: .
    env_file:
      - ./.env
```

This will load the environment variables from the .env file in the same directory as your `docker-compose.yml`.

Remember not to include your .env file in your Docker images, as this can expose your sensitive information. Instead, provide the environment variables at runtime or use secrets management tools for Docker.

### Google Cloud Functions

In Google Cloud Functions, you can set environment variables in the Google Cloud Console. In the function's settings, there's an "Environment variables" section where you can set key-value pairs.

### Heroku

In Heroku, environment variables are called Config Vars. You can set them in the Heroku Dashboard, under the "Settings" tab of your app.

### Kubernetes

In Kubernetes, environment variables can be set in the Pod configuration file:

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: my-pod
spec:
  containers:
  - name: my-container
    image: my-image
    env:
    - name: DATABASE_URL
      value: postgresql://localhost/mydatabase
    - name: SECRET_KEY
      value: my-secret-key
```

This will set the environment variables for all processes running in the containers of the Pod.

Always be sure to follow best security practices when handling sensitive information in your applications and services.