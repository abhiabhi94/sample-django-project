## A sample django project to start with more basic functionalities

A django project setup within minimum time. 

### Features

- Separate settings for production and development environment. In case, you want to read in detail about this, I wrote an article here: https://www.hackadda.com/post/2020/2/21/separate-your-development-and-production-settings-for-a-django-project

- The development server can also be accessible from outside the LAN(Local Area Network) on your desired port(`8000` being the example in this case) using this command.
    ```python
    python manage.py runserver 0.0.0.0:8000
    ```

    - **Note**
        - You need to set up port-forwarding and allow incoming connection to the port on your machine.

        - Use this only for **testing** purposes(this can cause security issues). 

- `SECURITY_KEY` and `DATABASE` credentials are never added by git (or any other version control software that you use).

### Setting up the project

- Clone this repository.

- Rename the parent directory(`sample-django-project`) as the name for your project.

- Rename the directory `sample-django-project` inside the parent directory as the name of your project.

- Just update the following keys the file `setup.json`.

    - `NAME` as name of your project.

    - `CONFIG_FILE` as the **absolute** location of the configuration file. 

        - This file will be used for reading the security key. Just add a `json` file(outside this project). Incase you want to use any other method, update [here](settings/__init__.py#L7). Just update the **absolute** location of this file inside `setup.json`  
            
            Format
            ```json
            {
                "SECRET_KEY": "my_secret_key"
            }
            ```
            - Note: For production environment, add a `PROD` key to the `config` file.

- See whether [.gitignore](./.gitignore) and [.LICENSE](./.LICENSE) file is according to your needs. Edit if required. 

- The project is now setup. Try to run the development server. If it works well, you may update this README file with your project's description.

- Don't forget to remove `.git` directory and reintialise it again using `git init` to allow `git` to track your project now.

#### This project was setup using Django 3.0.3, python 3.7.5