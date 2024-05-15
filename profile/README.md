<img width="1187" alt="Screenshot 2024-04-26 at 7 12 59 PM" src="https://github.com/oslabs-beta/OptiKube-FE/assets/78817053/cdc2c4bf-8f7c-44fb-b21d-94e2a68700ce">
<div align="center">
  
# OptiKube 

<p> Logo to go here or replace "optikube" above </p>

![Google Cloud](https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)
![Kubernetes](https://img.shields.io/badge/kubernetes-326ce5.svg?&style=for-the-badge&logo=kubernetes&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=for-the-badge&logo=Helm&labelColor=0F1689)
![Redis](https://img.shields.io/badge/redis-CC0000.svg?&style=for-the-badge&logo=redis&logoColor=white)
![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express%20js-000000?style=for-the-badge&logo=express&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-000000?style=for-the-badge&logo=prometheus&labelColor=000000)
![Grafana](https://img.shields.io/badge/Grafana-F2F4F9?style=for-the-badge&logo=grafana&logoColor=orange&labelColor=F2F4F9)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Next.js](https://img.shields.io/badge/Next.js-lightgray?style=for-the-badge&logo=next.js&logoColor=black)
![Javascript](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Tailwindcss](https://img.shields.io/badge/Tailwindcss-090e1a?style=for-the-badge&logo=tailwindcss)
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)


<p> Read about the process and work that went into building Optikube [here](medium.com)</p>

---

</div>




## Status
Optikube is currently in production stage but is set to launch soon!

## Table of Contents

- [Description](#description)
- [Features](#features)
- [Getting Started](#getting_started)
- [Installation](#installation)
- [Contributions](#contributions)
- [Creators](#creators)
- [Licsense](#license)


## Description
Welcome to OptiKube, an advanced open-source tool designed for Kubernetes users aiming to optimize and manage their cluster resources and costs effectively. OptiKube offers a comprehensive solution to efficient cluster management, enabling detailed cost and resource visualizations alongside automated scaling functionalities. By leveraging real-time data from services like Google Cloud Platform and integrating with KEDA for event-driven autoscaling, OptiKube ensures efficient resource utilization and cost management across Kubernetes deployments.

## Features
- Horizontal auto-scaler tool that implements event driven autoscaling based off user input.
- Automatic resource optimization for all OptiKube managed deployments each hour.
- Resource visualization such as RAM, memory, and CPU efficiency.
- Cost insights on a user's deployment utilizing real time data.
- **Event-Driven Autoscaling**
  - Integrates with Kubernetes Event-driven Autoscalers (KEDA) to dynamically adjust pod counts based on user-defined optimization settings and workload demands.
- **Automated Resource Optimization:**
  - Queries Kubecost data hourly to adjust resources, ensuring optimal performance and cost efficiency for OptiKube managed deployments.
- **Cost and Resource Visualizations:**
  - Provides comprehensive graphs and visuals that display cost breakdowns, resource usage, and resource efficiency across various deployments.
- **Scaler Management:**
  - Allows users to create, update, and delete KEDA scalers through the frontend interface.
- **User-Centric Optimization Settings**:
  - Enables users to specify optimization priorities, including application criticality and workload variability, focusing on either cost reduction or performance enhancement. 

## Getting Started
Before attempting to launch Optikube, the following should already be installed and running on your local machine:
- Helm Client installed ➡️ [Helm](https://helm.sh/docs/intro/install/)
- Kubectl installed ➡️ [Kubectl](https://kubernetes.io/docs/tasks/tools/#kubectl)
- A supported Kubernetes cluster deployed (currently only GKE) ➡️ [GKE](https://cloud.google.com/kubernetes-engine/docs/quickstarts/create-cluster)

## Installing OptiKube
**Step 1: Install OptiKube**
  - Running the following command will install OptiKube via Helm chart.
  ```
  helm repo add optikube https://optikube.github.io/optikube-helm-chart/ && \
  helm repo update && \
  helm install optikube optikube/optikube --namespace optikube --create-namespace
  ```
**Step 2: Enable port-forward**
  ```
  kubectl port-forward --namespace optikube deployment/optikube-dashboard 3000
  ```
**Step 3: Optimize your cluster!** :tada: 
  - You can now view the deployed frontend by visiting the following link.
  - [http://localhost:3000](http://localhost:3000)
  - Publish :3000 as a secure endpoint on your cluster to remove the need to port forward.

## Using OptiKube
With Optikube installed, you can immediately start to harness the full potential of your Kubernetes cluster:
  - Navigate to the frontend to view and analyze cost insights and resource usage.
  - Use the HPA dashboard to set up and adjust KEDA scalers according to your specific requirements and priorities.
  - Benefit from automatic adjustments to your deployments, ensuring efficient resource use and cost savings.

## Updating OptiKube
After installing OptiKube, you will be able to update your version with the following command:
  ```
  helm repo add optikube https://optikube.github.io/optikube-helm-chart/ && \
  helm repo update && \
  helm upgrade optikube optikube/optikube -n optikube
  ```
  
## Deleting OptiKube
After installing OptiKube, you will be able to update your version with the following command:
  ```
helm uninstall optikube -n optikube
  ```

## Contributions
Contributions play a vital role in the open-source community and would be welcomed! If you'd like to contribute to OptiKube please follow the steps below.
- Fork the project.
- Create and work off of your feature branch.
- Create a pull request with a detailed description of your changes using our template to merge your feature branch into dev.
- We will review it and get back to you!

## Creators

- **Cheryl Lee** <a href="https://github.com/yli-yanchen" target="blank"><img align="center" src="https://iconmonstr.com/wp-content/g/gd/makefg.php?i=../releases/preview/2012/png/iconmonstr-github-1.png&r=56&g=136&b=255" alt="github" height="30" width="30" /></a> <a href="https://www.linkedin.com/in/cherylleech/" target="blank"><img align="center" src="https://iconmonstr.com/wp-content/g/gd/makefg.php?i=../releases/preview/2012/png/iconmonstr-linkedin-3.png&r=56&g=136&b=255" alt="github" height="30" width="30" /></a>
- **James Shea** <a href="https://github.com/JamesSheaDev" target="blank"><img align="center" src="https://iconmonstr.com/wp-content/g/gd/makefg.php?i=../releases/preview/2012/png/iconmonstr-github-1.png&r=56&g=136&b=255" alt="github" height="30" width="30" /></a> <a href="https://www.linkedin.com/in/james-r-shea/" target="blank"><img align="center" src="https://iconmonstr.com/wp-content/g/gd/makefg.php?i=../releases/preview/2012/png/iconmonstr-linkedin-3.png&r=56&g=136&b=255" alt="github" height="30" width="30" /></a>
- **George Huang** <a href="https://github.com/gzfh24" target="blank"><img align="center" src="https://iconmonstr.com/wp-content/g/gd/makefg.php?i=../releases/preview/2012/png/iconmonstr-github-1.png&r=56&g=136&b=255" alt="github" height="30" width="30" /></a> <a href="https://www.linkedin.com/in/gzfh" target="blank"><img align="center" src="https://iconmonstr.com/wp-content/g/gd/makefg.php?i=../releases/preview/2012/png/iconmonstr-linkedin-3.png&r=56&g=136&b=255" alt="github" height="30" width="30" /></a>
- **Josh Bajarias** <a href="https://github.com/Jawshhhhhhhh" target="blank"><img align="center" src="https://iconmonstr.com/wp-content/g/gd/makefg.php?i=../releases/preview/2012/png/iconmonstr-github-1.png&r=56&g=136&b=255" alt="github" height="30" width="30" /></a> <a href="https://www.linkedin.com/in/joshbajarias/" target="blank"><img align="center" src="https://iconmonstr.com/wp-content/g/gd/makefg.php?i=../releases/preview/2012/png/iconmonstr-linkedin-3.png&r=56&g=136&b=255" alt="github" height="30" width="30" /></a>
- **Andy Guajardo** <a href="https://github.com/andymattgee" target="blank"><img align="center" src="https://iconmonstr.com/wp-content/g/gd/makefg.php?i=../releases/preview/2012/png/iconmonstr-github-1.png&r=56&g=136&b=255" alt="github" height="30" width="30" /></a> <a href="https://www.linkedin.com/in/andy-guajardo-a63987101/" target="blank"><img align="center" src="https://iconmonstr.com/wp-content/g/gd/makefg.php?i=../releases/preview/2012/png/iconmonstr-linkedin-3.png&r=56&g=136&b=255" alt="github" height="30" width="30" /></a>

## License
OptiKube is developed under the [MIT License](https://mit-license.org/).
