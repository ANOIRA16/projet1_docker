***DOCKER ESSENTIALS : CHEAT SHEET***

## Prerequisites🔗
    You need to have Docker Engine & Docker Compose installed 
    #To install Docker you need to install the following prerequisites
        ```sudo apt-get install curl
            sudo apt-get install gnupg
            sudo apt-get install ca-certificates
            sudo apt-get install lsb-release``` 

    #Then download the gpg file for Ubuntu
        ```sudo mkdir -p /etc/apt/keyrings
            curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg```

        ```echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-pluginsudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-pluginlinux/ubuntu   $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null```

