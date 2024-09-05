# Jenkins Agent with kubectl and helm

[![Docker Stars](https://img.shields.io/docker/stars/arunahq/jenkins-kubectl-inbound-agent.svg)](https://hub.docker.com/r/arunahq/jenkins-kubectl-inbound-agent)
[![Docker Pulls](https://img.shields.io/docker/pulls/arunahq/jenkins-kubectl-inbound-agent.svg)](https://hub.docker.com/r/arunahq/jenkins-kubectl-inbound-agent)

This Docker image is designed to deploy a Jenkins agent within a Kubernetes (K8s) cluster, specifically for executing `kubectl` and `helm` commands. It is ideal for use in CI/CD pipelines that require interaction with Kubernetes resources and Helm charts.

The image is built upon Jenkins' official **[jenkins/inbound-agent](https://hub.docker.com/r/jenkins/inbound-agent/)** image, ensuring compatibility with Jenkins server setups that utilize inbound agents for workload distribution.

**Note:** The legacy Jenkins agent images **[jenkinsci/jnlp-slave](https://hub.docker.com/r/jenkinsci/jnlp-slave)** and **[jenkins/jnlp-slave](https://hub.docker.com/r/jenkins/jnlp-slave)** are deprecated and should no longer be used. Transition to newer images like `jenkins/inbound-agent` for better support and security.

