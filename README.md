# struts-showcase
This repo contains the code for the Struts2 showcase web app (v2.5.28) and includes several CI/CD scripts to demonstrate scanning the .war build artifact with ReversingLabs.

**Jenkinsfile**

A Jenkins pipeline script that builds the WAR, scans it with the [ReversingLabs CLI](https://docs.secure.software/cli/), and publishes the reports in HTML, JSON, and CycloneDX formats. This script is for a setup where the RL CLI has been installed on a persistent instance of Jenkins.

**Jenkinsfile_docker**

A Jenkins pipeline script that builds the WAR, scans it using the [ReversingLabs Docker image](https://hub.docker.com/r/reversinglabs/rl-scanner), and publishes the reports in HTML, JSON, and CycloneDX formats. Using the Docker image is ideal for an emphemeral instance of Jenkins.

**azure-pipelines.yml**

An Azure DevOps pipeline script that builds the WAR and scans it with the ReversingLabs CLI. The [rl-deploy](https://pypi.org/project/rl-deploy/) Python package is installed and subsequently used to install and license the CLI. Scan reports in HTML, JSON, and CycloneDX formats are published as pipeline artifacts.