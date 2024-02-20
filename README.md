# Liatrio Go API

This is a simple dockerized go application that will return a `json` blob when you `curl` it on the main path `/`. 

The API will return a `404` if any other path is used like `/error`. 

The API will also return a `200` and `'success': true`  for `/healthcheck` once running.

The default port API is bound to is on port `5000`. You can update this by editing [this line](https://github.com/b1tsized/go-liatrio/blob/main/main.go?plain=1#L29) and update [this line](https://github.com/b1tsized/go-liatrio/blob/main/Dockerfile?plain=1#L7).

## Running locally

1. Clone the repo:

    ```bash
    git clone https://github.com/b1tsized/go-liatrio
    ```

2. `cd` into the directory:

    ```bash
    cd ./go-liatrio
    ```
   
3. Build the Docker Image:

    ```bash
   docker build . -t liatrio-go
   ```

4. Run the Docker Container:

    ```bash
    docker run -d -p 8080:5000 liatrio
    ```
5. `curl` your local machine to see if you get a valid response:

    ```bash
    curl http://localhost
    ```
