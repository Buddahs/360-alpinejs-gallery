-[0_-]- 
> "Simplicity has a meaning for a reason"
### [INIT]
```shell
npm install
```
### [RUN]
```shell
npm start
npm run dev
```

## Three.js Application Setup

This project includes a simple Three.js application that runs inside a Docker container.

### Prerequisites

- Docker: Make sure you have Docker installed and running on your system. You can download it from [https://www.docker.com/get-started](https://www.docker.com/get-started).
- Docker Compose (usually included with Docker Desktop).

### Running the Three.js Application

1.  **Navigate to the project root directory:**
    Open your terminal or command prompt and change to the directory where this `README.md` file is located.

2.  **Build and run the container using Docker Compose:**
    ```bash
    docker-compose up --build
    ```
    The `--build` flag ensures the Docker image is built (or rebuilt if changes were made to the Dockerfile or application files in `threejs_app`).

3.  **Access the application:**
    Open your web browser and go to [http://localhost:8080](http://localhost:8080). You should see a spinning green cube.

4.  **To stop the application:**
    Press `Ctrl+C` in the terminal where `docker-compose up` is running.
    To remove the container (and network if created), you can run:
    ```bash
    docker-compose down
    ```

### Project Structure

-   `threejs_app/`: Contains the Three.js application files.
    -   `index.html`: The main HTML file.
    -   `main.js`: The JavaScript file with the Three.js code.
    -   `Dockerfile`: Defines how to build the Docker image for the Three.js app.
-   `docker-compose.yml`: Defines the Docker Compose services to easily build and run the application.

This setup is separate from the existing Node.js/Express application in the repository.
