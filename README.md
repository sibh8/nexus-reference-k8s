# nexus-reference-k8s

This project will capture the process of the creation and refinement K8s resources for th Nexus platform. The idea is to start with docker-compose and use the Kompose project to convert the docker definition into k8s, Helm, and Openshift templates. From there we will document how we've evolved those base templates.

The real goal for me is to convert my demo environment from docker-compose to one the runs in Kubernetes, or OpenShift v4. While Helm might be enough for my own work I'll try to push this to explore real world customer deployments.
