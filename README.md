**Docker Hello World**

*Create your first docker container and upload the image*

Run the following to create a your first docker container

- `docker build -t friendlyhello .` // Build the docker in a linux container
- `docker run -p 4000:80 friendlyhello` // Run your application

Notes
- You should see a message that Python is serving your app at http://0.0.0.0:80. But that message is coming from inside the        container, which doesn’t know you mapped port 80 of that container to 4000, making the correct URL http://localhost:4000.
- Go to that URL in a web browser to see the display content served up on a web page.


*Now let’s run the app in the background, in detached mode:*

- `docker run -d -p 4000:80 friendlyhello`

*To stop the cotainer*

- `docker container stop 1fa4ab2323` - {container Id}

* Share your image

- Run docker tag image with your username, repository, and tag names so that the image uploads to your desired destination. The    syntax of the command is: `docker tag image username/repository:tag`

*To see the image you created*
- `docker image ls`

*Push your image to the repository*
- `docker push username/repository:tag`

*Pull and run the image from the remote repository*
- `docker run -p 4000:80 username/repository:tag`


* Created by Sonu Jose
