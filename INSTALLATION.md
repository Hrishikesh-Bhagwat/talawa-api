# Installation

Talawa API can be setup to run via `Docker` or node's default package manager `Npm`.

## Docker

Follow these steps to get the api running using docker

1. Install these dependencies if you don't already have them
   - [Docker](https://docs.docker.com/engine/install/)
   - [Nodejs](https://nodejs.org/en/)
2. Clone this repo to your local machine

   ```sh
   git clone https://github.com/PalisadoesFoundation/talawa-api
   cd talawa-api
   ```

3. Create `.env` file in the root directory of the project
   `.env` file is used to store the secret or environment variables.

   ```sh
   touch .env
   ```

4. Copy the `.env.sample` to `.env`

5. You will have to set these variables in `.env` to provide the necessary secrets and connection url.

   Please follow instructions in the comments at the top of `.env`.

   - ACCESS_TOKEN_SECRET
   - REFRESH_TOKEN_SECRET
   - MONGO_DB_URL

6. Now that the enviornment variables are setup. Run the following commands in the terminal.

   This command will build the docker image.

   ```sh
   sudo docker-compose build
   ```

   This command will run the container, just use the following command to run the server in future.

   ```sh
   sudo docker-compose up
   ```

## Standard Installation

Follow these steps to get the api running using npm

1. Install these dependencies if you don't already have them
   - [MongoDB](https://docs.mongodb.com/manual/administration/install-community/)
   - [Nodejs](https://nodejs.org/en/)
2. Clone this repo to your local machine

   ```sh
   git clone https://github.com/PalisadoesFoundation/talawa-api
   cd talawa-api
   npm install
   ```

3. Create `.env` file in the root directory of the project
   `.env` file is used to store the secret or environment variables.

   ```sh
   touch .env
   ```

4. Copy the `.env.sample` to `.env`

5. Fill out the following fields:

   - ACCESS_TOKEN_SECRET
   - REFRESH_TOKEN_SECRET
   - MONGO_DB_URL

     Follow instructions in the comments at the top of `.env`

6. Install required node packages

   ```sh
   npm install
   ```

7. Now that we have all the packages, execute the following command to run the server.

   NB: You only have to execute the following command to run the server in future.

   ```sh
   npm run start
   ```

## Testing

```sh
npm run test
```

### Standard Installation vs Docker

Docker downloads a lot of large images, if you are short on storage or with slow internet connection prefer using standard development installation.
