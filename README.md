1.Setup EC2 Instance:
Launched an Ubuntu EC2 instance and installed Docker and Node.js.

2.Created Node.js App:
Built a simple index.js app with package.json and tested it locally using node index.js.

3.Dockerized the App:
Created a Dockerfile to containerize the Node.js app.
Built the image using docker build -t my-node-app . and ran it with docker run -d -p 3000:3000 my-node-app.

4.Configured GitHub Actions:
Added a CI/CD pipeline in .github/workflows/main.yml for building and pushing the Docker image to DockerHub automatically.

5.DockerHub Integration:
Added DockerHub credentials (DOCKERHUB_USERNAME, DOCKERHUB_TOKEN) as GitHub Secrets.
Each push to the main branch triggers a workflow that builds and pushes the latest image to Dockerhub

5.Deployed on EC2:
Verified the app running at http://<EC2-Public-IP>:3000.
