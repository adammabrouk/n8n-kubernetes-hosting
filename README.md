# n8n-kubernetes-hosting

Get up and running with n8n on the following platforms:

* [AWS](https://docs.n8n.io/hosting/server-setups/aws/)
* [Azure](https://docs.n8n.io/hosting/server-setups/azure/)
* [Google Cloud Platform](https://docs.n8n.io/hosting/server-setups/google-cloud/)

If you have questions after trying the tutorials, check out the [forums](https://community.n8n.io/).

## Prerequisites

Self-hosting n8n requires technical knowledge, including:

* Setting up and configuring servers and containers
* Managing application resources and scaling
* Securing servers and applications
* Configuring n8n

n8n recommends self-hosting for expert users. Mistakes can lead to data loss, security issues, and downtime. If you aren't experienced at managing servers, n8n recommends [n8n Cloud](https://n8n.io/cloud/).

## Dependencies for GKE

Before deploying n8n on GKE, ensure you have the following dependencies set up:

* A static IP address
* A managed certificate
* A GKE cluster with sufficient resources
* Helm installed on your local machine

## Full Setup Process for GKE

Follow these steps to set up and deploy n8n on GKE using Helm:

1. **Create a GKE Cluster**: 
   - Create a GKE cluster with sufficient resources to run n8n.
   - Ensure the cluster has access to a static IP address and a managed certificate.

2. **Set Up Static IP and Managed Certificate**:
   - Reserve a static IP address in your GCP project.
   - Create a managed certificate for your domain.

3. **Install Helm**:
   - Install Helm on your local machine if you haven't already.
   - Initialize Helm in your GKE cluster.

4. **Clone the Repository**:
   - Clone the `n8n-kubernetes-hosting` repository to your local machine.

5. **Configure Helm Chart**:
   - Navigate to the `n8n-kubernetes-hosting` directory.
   - Edit the `values.yaml` file to set your specific values for template variables.

6. **Deploy with Helm**:
   - Run `helm install n8n ./` to deploy n8n using the Helm chart.

7. **Verify Deployment**:
   - Check the status of your deployment using `kubectl get all -n n8n`.
   - Ensure all pods are running and services are correctly configured.

8. **Access n8n**:
   - Access n8n using the domain associated with your managed certificate and static IP address.

## Contributions

For common changes, please open a PR to `main` branch and we will merge this
into cloud provider specific branches.

If you have a contribution specific to a cloud provider, please open your PR to
the relevant branch.
# n8n-kubernetes-hosting
