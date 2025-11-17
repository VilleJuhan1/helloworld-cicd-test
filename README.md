# A modified Hello World app for CI/CD testing

Components:

- index.js and package.json for the Javascript code
- Dockerfile for building the image
- Github workflow for building and pushing the app to Docker Hub
- Docker-compose file for Watchtower

## Usage

1. Fork project and setup the necessary secrets to the repository. Pull the project, make some changes and see if the Docker pipeline works
2. Create an .env file and add your newly created image there.
3. Next, spin up the two containers:

```bash
docker compose up
```

Open your browser and check localhost:8080. It should show "Hello World!" Make a change to the text in the index.js file. Commit the changes and wait for five minutes. Reload the browser page. Watchdog should've pulled and used the latest image and the changes should be visible on the app.
