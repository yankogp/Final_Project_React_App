DevOps upskill final project

The project contains simple react application

The project contain CI/CD workflow

The repository contains following files:
-	CI.yaml – workflow file for github actions
-	Application folders - /public and /src
-	Application files - package-lock.json and package.json
-	Dockerfile – needed to be created docker image
-	.gitignore – ignore some items from Source control
-	Trivy.yaml – neede for security scanner
-	Terraform folder – terraform files for creating EKS cluster on AWS

The Github actions workflow is are follow:

-	Check repository
-	Setup Node.js  - needed for React application build
-	Gitleaks_test
-	Trivy vulnerability scanner
-	Build Docker image and push to repository
-	build on feature branches, push only on main branch
-	Trivy docker image scanner
-	Update deployment.yaml with latest docker image tag

-	The deployment is organized with ArgoCD over Kubernetes Kluster
