# NoSQL Platform on Docker

## Provisioning environment
The environment for this course is completly based on docker containers. 

In order to simplify the provisioning, a single docker-compose configuration is used. All the necessary software will be provisioned using Docker. 

You have the follwing options to start the environment:

 * [**Local Virtual Machine Environment**](./LocalVirtualMachine.md) - a Virtual Machine with Docker and Docker Compose pre-installed will be distributed at by the course instructure. You will need 50 GB free disk space.
 * [**Local Docker Enironment**](./LocalDocker.md) - you have a local Docker and Docker Compose setup in place which you want to use
 * [**AWS Lightsail Environment**](./Lightsail.md) - AWS Lightsail is a service in Amazon Web Services (AWS) with which we can easily startup a environment and provide all the necessary bootstraping as a script.


## Post Provisioning

These steps are necessary after the starting the docker environment. 

### Add entry to local /etc/hosts File
To simplify working with the Analytics Platform and for the links below to work, add the following entry to your local `/etc/hosts` file. 

```
40.91.195.92	analyticsplatform
```

Replace the IP address by the PUBLIC IP of the docker host. 

## Services accessible on Analyticsplatform Platform
The following service are available as part of the platform:

Product | Type | Service | Url
------|------| --------| ----
Hue | Development | Hue | <http://analyticsplatform:28888>
Zepplin | Development | Zeppelin | <http://analyticsplatform:38081>
Jupyter | Development | Jupyter | <http://analyticsplatform:38888>
Spark UI | Management  | Spark | <http://analyticsplatform:8080>
Spark History Server UI | Management | Spark | <http://analyticsplatform:18080>
Namenode UI | Management  | Haoop HDFS | <http://analyticsplatform:50070>
Datanode-1 UI | Management  | Haoop HDFS | <http://analyticsplatform:50075>
Datanode-2 UI | Management  | Haoop HDFS | <http://analyticsplatform:50076>
Kafka Manager | Management | Kafka | <http://analyticsplatform:29000>
Minio UI | Management | Minio | <http://analyticsplatform:9000>

