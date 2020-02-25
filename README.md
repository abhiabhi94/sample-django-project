## A sample django project to start

### Features

- Separate settings for production and development environment.

- `SECURITY_KEY` and `DATABASE` credentials are never uploaded to github.

### Setting up the project

- Clone this repository.

- Rename the parent directory(`sample-django-project`) as the name for your project.

- Rename the directory `sample-django-project` inside the parent directory as the name of your project.

- Just update the following keys the file `setup.json`.

    - `NAME` as name of your project.

    - `CONFIG_FILE` as the **absolute** location of the configuration file. 

        - This file will be used for reading the security key. Just add a `json` file(outside this project). Incase you want to use any other method, update [here](settings/__init__.py#L7). Just update the **absolute** location of this file inside `setup.json`  
            
            Format
            ```
            {
                "SECRET_KEY": "my_secret_key"
            }
            ```
            - Note: For production environment, add a `PROD` key to the `config` file.

- See whether [.gitignore](./.gitignore) file is according to your needs. Edit if required. 

- The project is now setup. Try to run the development server. If it works well, you may update this README file with your project's description.

- Don't forget to remove .git and reintialise it again using `git init` to keep it track of your project now.

#### This project was setup using Django 3.0.3, python 3.7.5