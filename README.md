![code coverage badge](https://github.com/boobooboo-dum1/learn-cicd-starter/actions/workflows/ci.yml/badge.svg)

# learn-cicd-starter (Notely)

This repo contains the starter code for the "Notely" application for the "Learn CICD" course on [Boot.dev](https://boot.dev).

## Local Development

Make sure you're on Go version 1.22+.

Create a `.env` file in the root of the project with the following contents:

```bash
PORT="8080"
```

Run the server:

```bash
go build -o notely && ./notely
```

*This starts the server in non-database mode.* It will serve a simple webpage at `http://localhost:8080`.

You do *not* need to set up a database or any interactivity on the webpage yet. Instructions for that will come later in the course!

# Lesson

## update README 

Just some update on the README

## Docker cmd

Build binary
```bash
./scripts/buildprod.sh
``` 

Build docker image
```bash
docker build -t emmaqu/notely:latest .
``` 

Run docker image
```bash
docker run -e PORT=8080 -p 8080:8080 emmaqu/notely:latest
``` 

## Send to GCP Artifact Registry

```bash
gcloud builds submit --tag us-central1-docker.pkg.dev/notely-426920/notely-ar-repo/notely:latest .
``` 