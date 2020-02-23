# Welcome to go-docker

This is a sample repository displaying containerization of go applications with external dependencies using Docker. 

1. Check out this repository
2. Install and run docker on your machine
3. Run the below commands in the order

This step builds an image for our go applciation using the docker file

```sh
docker build -t go-docker-app .
```

Check if your image has been created successfully using the below command, you should see 'go-docker-app' under REPOSITORY column

```sh
docker images
```

Next execute the below command to run the image we just created (this command is exposing our go application running on port '8000' inside our container to the port '8080' on our local machine)

```sh
docker run -p 8080:8000 -it go-docker-app
```

Now if you open your browser and go to http://localhost:8080/ you should see our application running. 

Happy Coding!