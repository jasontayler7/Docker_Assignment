DAY 6 Docker

Assignment
Install docker-compose on your machine, if not already installed.

        ```
        $ sudo curl -L https://github.com/docker/compose/releases/download/1.21.2/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
        $ sudo chmod +x /usr/local/bin/docker-compose
        ```
![Docker installed]()

Check docker-compose version.

        ```
        $ docker-compose --version
        ```
![docker version]()

Create a directory named nginx in your root.

        ```
        $ mkdir nginx
        ```
![nginx created]()




Switch to that directory and create a file named docker-compose.yaml

       ```
        $ mkdir nginx
        ```
![nginx created]()

Use docker-compose version 2 to create docker-compose.yaml file.

Create a service named "databases".

Use image named "mysql"

Map container 3306 port to host machine 3306 port.

Add environment variables named "MYSQL_ROOT_PASSWORD", "MYSQL_DATABASE", 

"MYSQL_USER" and "MYSQL_PASSWORD" along with corresponding values for all.

Add another service named "web"

Use image "nginx"

Save docker-compose.yaml file and do docker-compose up.

       ```
       version: '2'
       services:
         databases:
         image: "mysql"
         ports:
            - "3306:3306"
         environment:
            - MYSQL_ROOT_PASSWORD=123
            - MYSQL_DATABASE=lovedeep_sharma
            - MYSQL_USER=root
            - MYSQL_PASSWORD=123

        web:
        image: nginx
        ports:
            - "80:80"
        depends_on:
            - databases

    ...
       ```

![docker-compose-file]()

Verify nginx service is up and is accessible on machine.

![nginx-verification]()

Stop and remove your docker container using docker-compose.

        ```
         $ docker-compose down
        ```

![docker-compose-down]()
