***DOCKER ESSENTIALS : CHEAT SHEET***

## Essential commands to never forget🔗
    sudo docker --version
    docker compose version
    sudo docker ps -a
    sudo docker images

## Prerequisites🔗
    You need to have Docker Engine & Docker Compose installed 
    #To install Docker you need to install the following prerequisites
        sudo apt-get install curl
        sudo apt-get install gnupg
        sudo apt-get install ca-certificates
        sudo apt-get install lsb-release

    #Then download the gpg file for Ubuntu
        sudo mkdir -p /etc/apt/keyrings
        curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

        echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-pluginsudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-pluginlinux/ubuntu   $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
        sudo apt-get update
        sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
    
    #Test the installation with the following command
        sudo docker run hello-world
### Then, add your python logic in "app.py"
    create your route with a function for @app.route('/'), default port or redis is 6379, search what port is displayed on the browser
### Requirements should be in a file named requirements.txt
    flask
    redis
### add a file named Dockerfile and make your code work 
    main commands inside the file are :
    FROM 
    WORKDIR
    ENV
    RUN
    COPY
    EXPOSE
    CMD

## After having successfully installed docker compose, Make a new file called "docker-compose.yml"
    Inside of which you need to paste the following code :
    ``` version: "3.9"
        services:
        web:
            build: .
            ports:
            - "8000:5000"
        redis:
            image: "redis:alpine"```


### BUILD AND RUN WITH A SIMPLE COMMAND 
    Use ```sudo docker compose up``` to pull a Redis image, builds an image for your code, and starts the services you defined. In this case, the code is statically copied into the image at build time.

    type the ip with the corresponding port and you should see the result.

    Use ```sudo docker compose down``` to stop the images
    check docker compose help for more
    docker compose down --volumes
### You need to install the rootless mode to stop adding sudo to your commands
    You can do so by running the following code in your terminal
    ``` dockerd-rootless-setuptool.sh install
        sudo apt-get install -y docker-ce-rootless-extras```

# VISIT THE DOCKER HUB FOR MORE...
