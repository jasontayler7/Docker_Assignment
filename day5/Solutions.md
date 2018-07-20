DAY 4 Docker

Assignment
Signup on dockerhub. 

       ![Dockerhub login]()

Login on dockerhub and create a repository by providing repo name "mytestrepo" and a little description about the same.

       ![mytestrepo]()
 
Search for "centos" image on docker using commandline.

        ```
        $ sudo docker search centos
        ```
 
        ![docker search]()

Limit out search result to 10 entries only. 

        ```
         $ sudo docker search centos --limit 10
        ```

        ![docker search limit]()

Apply a filter on search result to show entries for images having 3 stars. 

        ```
         
        ```

       ![docker filter]()

Format the search result to get output containing only name,description and is_official values. 

        ```
        $ sudo docker search --format "{{.Name}}:{{.Description}}:{{.IsOfficial}}" centos
        ```

        ![docker format]()

Pull an image named "centos" from dockerhub. 

       ```
       $ sudo docker pull centos
       ```

       ![docker pull]()

Tag "centos" image with name "mycentos" in your repository with version 1.1 

       ```
       $ sudo docker image tag centos lovedeep/mycentos:v1.1
       ```

       ![docker tag]()

Push that image to your repo "mytestrepo" on your dockerhub. 

       ```
       $ sudo docker push lovedeep/mycentos:v1.1
       ```

       ![docker login]()

       ![docker push]()

Do commandline logout on dockerhub. 

       ```
       $ sudo docker logout
       ```


![docker logout]()
