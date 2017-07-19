# hello-docker
This is just a simple intro into [Docker](https://www.docker.com/). To use this repo to create a [Docker image](https://docs.docker.com/engine/reference/commandline/images/), all you have to do is the following:

 * Clone this repo.
 * Build the image with the following command: `$ docker build -t <name_you_want_to_give_to_the_image> .`
 * Run the image with the following command: `$ docker run -p 49160:8080 -d <name_you_gave_to_the_image>`
 * `$ docker ps` to show that the image is infact running.
 * Navigate to your Docker machine on port 49160 and you will see the "Hello world" message!


### Quick notes
If you want to see the output of the app:
```
# Get container ID
$ docker ps

# Print app output
$ docker logs <container id>

# Example
Running on http://localhost:8080
```

If you want to get inside the container you can use the `exec` command:
```
# Enter the container
$ docker exec -it <container id> /bin/bash
```
