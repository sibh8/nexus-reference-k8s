# Nexus IQ Helm Chart

The Helm chart installs Nexus IQ as a service in Kubernetes cluster

## Chart Details
- The chart will expose the service on the default port 8070
- The chart provides license installation provision through init containers.

## Creation of licence init container pod
Once the license file is retrieved from Sonatype, a docker image needs to be built in which the licensefile will be stored as /etc/nexus-iq-server/license.lic

Sample of the docker file is as below

```
FROM centos:7

RUN mkdir /etc/nexus-iq-server/

COPY *.lic /etc/nexus-iq-server/license.lic

RUN chmod -R 744 /etc/nexus-iq-server/license.lic

CMD ["bash"]

```

## Installing the helm chart
Navigate inside the helm directory and execute the following command

```
helm install --name <Release-Name> nexusiq
```

## Configuration
| Parameter | Description | Default Value |
|---|---|---|
| `namespace` | Kubernetes namespace | `default` |
| `image.repository` | Nexus IQ image repository | `sonatype/nexus-iq-server` |
| `image.tag` | Tag associated with the image | `latest` |
|`image.pullPolicy` | The image pull policy | `Always` |
