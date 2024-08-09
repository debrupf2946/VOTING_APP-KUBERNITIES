# Voting App

This project is a microservices-based voting application deployed using Kubernetes. The app allows users to vote, processes those votes, and displays the results in real-time. The architecture includes multiple services, each running in its own Kubernetes pod, to ensure scalability, resilience, and ease of management.

## Architecture Overview

The Voting App is composed of five main microservices, each running in a separate pod:

1. **Voting Server**: A frontend application that allows users to cast their votes.
2. **Voting Result Server**: A backend service that displays the results of the voting in real-time.
3. **Redis**: An in-memory data structure store used to store votes temporarily.
4. **Worker Pod**: A background worker responsible for processing the votes from Redis and saving them to the Postgres database.
5. **Postgres**: A relational database used to store the final voting results.

Each service is deployed as a Kubernetes deployment and exposed using Kubernetes services.

## Prerequisites

- [Docker](https://www.docker.com/get-started) installed locally
- [Kubernetes](https://kubernetes.io/) cluster setup (e.g., Minikube, EKS, GKE, etc.)
- [Kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/) command-line tool configured to interact with your Kubernetes cluster
- [Helm](https://helm.sh/) installed for managing Kubernetes applications (optional)

