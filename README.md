# ESDE_WORKSHOP_TASK_CICD

## Requirements to Start working

### Pull Docker Image
Step 1 - Pull the Container: <br>
In the Repository root run: <br>
docker pull ellimen/esd:starter
<br>
If you get the error "no matching manifest for linux/arm64/v8 in the manifest list entries" you have to force pull with linux.
Run: <br>
docker pull --platform=linux/amd64 ellimen/esd:latest
Step 2 - Run the container: <br>
In the Repository root run: <br>
docker run --rm -p 8080:8080 -e APP_COMMIT=starter ellimen/esd:starter
Step 3 - Check that the container is healthy: <br>

curl -fsS http://localhost:8080/api/health
curl -fsS http://localhost:8080/api/info


## Task 1

<!-- Build & Deploy -->
<h2>CI Test Build</h2>

[![CI](https://img.shields.io/github/actions/workflow/status/janneshatzius/ESDE_WORKSHOP_TASK_CICD/CI.yml?branch=main)](https://github.com/janneshatzius/ESDE_WORKSHOP_TASK_CICD/actions/workflows/CI.yml)
<br>

<h2>CD Test Build</h2>

[![CD](https://img.shields.io/github/actions/workflow/status/janneshatzius/ESDE_WORKSHOP_TASK_CICD/CD.yml?branch=main)](https://github.com/janneshatzius/ESDE_WORKSHOP_TASK_CICD/actions/workflows/CD.yml)
<br>

<h2>Coverage of Tests</h2>

<!-- Coverage (Codecov) – will turn green once Codecov is set below -->

[![codecov](https://codecov.io/gh/janneshatzius/ESDE_WORKSHOP_TASK_CICD/graph/badge.svg?token=O77MK9D3UC)](https://codecov.io/gh/janneshatzius/ESDE_WORKSHOP_TASK_CICD)
<br>
<h2>Docker Pulls</h2>

<!-- Docker pulls (optional) -->
[![Docker Pulls](https://img.shields.io/docker/pulls/ellimen/esd)](https://hub.docker.com/r/ellimen/esd)
