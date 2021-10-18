## 1. Wellness App
Django Backend for the wellness app

### 8. Running the Django application locally by cloning the GitHub repository:
1. Clone this repository
2. Create a project on [infura](https://infura.io/) and get the project ID.
3. Set up with [Slate](https://slate.host/):
    - Sign Up.
    - Get the developer API key.
    - Create a Slate.
    - Get the Slate ID.
4. Then, create a Python virtual environment, and activate it:
    - run the following command within the cloned repository `virtualenv <your_env_name>`
    - and then run `source <your_env_name>/bin/activate`
5. Export the following environment variables (note: you can change the `rinkeby` to `ropsten` or `mainnet` if you are using those chains) by running the following commands:
    - `export AQUARIUS_URL=https://aquarius.rinkeby.oceanprotocol.com`
    - `export ENV_TYPE=local_test` (if you change it to deployment, follow the **step 7**)
    - `export NETWORK_URL=https://rinkeby.infura.io/v3/<your_infura_project_id>/`
    - `export PROVIDER_URL=https://provider.rinkeby.oceanprotocol.com`
    - `export SLATE_AUTH_CODE=<your_slate_developer_api_key>`
    - `export SLATE_ID=<the_id_of_the_slate_that_you_created>`
6. Install the requirements onto your virtual environment by using `pip3 install -r requirements.txt`
7. _ (Optional) If you’ve set the ENV_TYPE as production, and you are using a Postgres database, please export the following environment variables: _
    - `export DB_HOST=<your_database_host_address>`
    - `export DB_NAME=<name_of_your_database>`
    - `export DB_PORT=<the_port_of_your_PostgreSQL_database>`
    - `export DB_USER=<database_user_name>`
    - `export DB_PASS=<password_of_the_database_user>`
8. Run the following commands to make database migrations:
    - `python3 manage.py makemigrations`
    - `python3 manage.py migrate`
9. Run the Django server on your localhost at port 8000 by using the command: `python3 manage.py runserver`
