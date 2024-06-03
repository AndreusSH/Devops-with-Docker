## EXERCISE 1.3: SECRET MESSAGE
Now that we've warmed up it's time to get inside a container while it's running!

Image devopsdockeruh/simple-web-service:ubuntu will start a container that outputs logs into a file. Go inside the running container and use tail -f ./text.log to follow the logs. Every 10 seconds the clock will send you a "secret message".

Submit the secret message and command(s) given as your answer <br>
1. I start a container with -d detach flag so that the container runs in the background<br>
`docker run -d --name secret-message-container devopsdockeruh/simple-web-service:ubuntu` <br>
2. I open an interactive bash session within my container <br>
`docker exec -it secret-message-container bash`<br>
3. I follow logs in real time <br>
`tail -f ./text.log` <br>

`Secret message is: 'You can find the source code here: https://github.com/docker-hy'`