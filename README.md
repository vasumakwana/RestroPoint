# RestroPoint: A Restaurant Management App

A comprehensive Restaurant Management Application built with NodeJS, MySQL, and ReactJS.

### Built With

- [ReactJS](https://reactjs.org/)
- [NodeJS](https://nodejs.org/)
- [MySQL](https://www.mysql.com/)

### Installation

#### Manual Setup

1. **Clone the Repository**

    ```sh
    git clone https://github.com/vasumakwana/RestroPoint.git
    ```

2. **Install MySQL Server**

    Download and install a [MySQL Server](https://www.mysql.com/).

3. **Backend Configuration**

    Navigate to the `backend` directory and install the required dependencies.

    ```sh
    cd backend
    npm install
    ```

    Copy the `.env.example` file to `.env` and set the environment variables according to your database configuration.

    ```plaintext
    NODE_ENV=development
    PORT=5000
    JWT_SECRET=[YOUR SECRET]
    DB_USER=[DATABASE USER]
    DB_NAME=[DATABASE NAME]
    DB_PASSWORD=[DATABASE PASSWORD]
    DB_HOST=[DATABASE HOST]
    DB_DIALECT=mysql
    ```

    Initialize the database by running the following commands. The first command sets up the database structure, and the second populates it with initial data.

    ```sh
    npx sequelize-cli db:migrate
    npx sequelize-cli db:seed:all
    ```

4. **Start Backend Server**

    ```sh
    npm run dev
    ```

5. **Frontend Configuration**

    Navigate to the `frontend` directory and install the dependencies.

    ```sh
    cd ../frontend
    npm install
    ```

    Set up a proxy for the API requests by adding the following line to the `package.json` file in the `frontend` directory. More information about proxies can be found [here](https://create-react-app.dev/docs/proxying-api-requests-in-development/).

    ```json
    "proxy": "http://localhost:5000"
    ```

6. **Start Frontend Server**

    ```sh
    npm start
    ```

By following these steps, you should have the Restaurant Management App up and running on your local machine. If you encounter any issues or have further questions, feel free to open an issue on the GitHub repository. Enjoy managing your restaurant with ease!
