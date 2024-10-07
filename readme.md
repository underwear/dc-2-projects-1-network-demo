# dc demo

#### Step 1

Clone the repository:

```sh
git clone git@github.com:underwear/dc-2-projects-1-network-demo.git
```

Then navigate to the newly created folder:

```sh
cd dc-2-projects-1-network-demo
```

#### Step 2

Start the main project:

```sh
docker-compose -f main-project/docker-compose.yml up -d
```

#### Step 3

Run the "client" container in the second project and send a request to http://main-project-app:

1. Launch the `second-project-client` container with an open `sh` shell:
    ```sh
    docker-compose -f second-project/docker-compose.yml run --rm -t second-project-client sh
    ```
   
2. Send a test HTTP request to `http://main-project-app`
    ```shell
    curl http://main-project-app
    ```