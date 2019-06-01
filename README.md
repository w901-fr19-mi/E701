[1]: https://www.tuxcademy.org/download/de/lxes/lxes-de-manual.pdf
[7]: https://www.tuxcademy.org/

# ![](https://www.lpice.eu/fileadmin/_processed_/csm_LPIC-DevOpsToolsEngineer_43de3c4735.jpg) Exam 701: DevOps Tools Engineer 

### Topics

* [Topic 701: Software Engineering](#topic-701-software-engineering)
* [Topic 702: Container Management](#topic-702-container-management)
* [Topic 703: Machine Deployment](#topic-703-machine-deployment)
* [Topic 704: Configuration Management](#topic-704-configuration-management)
* [Topic 705: Service Operations](#topic-705-service-operations)
* [Bonusmaterial](#bonusmaterial)

## Topic 701: Software Engineering

### 701.1 Modern Software Development 
*** 

> [⇧ **Nach oben**](#topics)

**Weight**: 6 + 4 Bonuspunkte für die Erstellung eines Microservices inkl. Unit-Tests

**Description**: Candidates should be able to design software solutions suitable for modern runtime environments. Candidates should understand how services handle data persistence, sessions, status information, transactions, concurrency, security, performance, availability, scaling, load balancing, messaging, monitoring and APIs. Furthermore, candidates should understand the implications of agile and DevOps on software development.

Key Knowledge Areas:
* Understand and design service based applications
* Understand common API concepts and standards
* Understand aspects of data storage, service status and session handling
* Design software to be run in containers
* Design software to be deployed to cloud services
* Awareness of risks in the migration and integration of monolithic legacy software
* Understand common application security risks and ways to mitigate them
* Understand the concept of agile software development
* Understand the concept of DevOps and its implications to software developers and operators

The following is a partial list of the used files, terms and utilities:
* REST, JSON
* Service Orientated Architectures (SOA)
* Microservices
* Immutable servers
* Loose coupling
* [Cross site scripting](https://www.owasp.org/index.php/Cross-site_Scripting_(XSS)), [SQL injections](https://www.owasp.org/index.php/SQL_Injection), verbose error reports, API authentication, consistent enforcement of transport encryption
* [CORS headers](https://de.wikipedia.org/wiki/Cross-Origin_Resource_Sharing) and [CSRF tokens](https://de.wikipedia.org/wiki/Cross-Site-Request-Forgery)
* [ACID](https://de.wikipedia.org/wiki/ACID) properties and [CAP theorem](https://de.wikipedia.org/wiki/CAP-Theorem)

**Unterlagen**

[![](https://img.youtube.com/vi/PH4HtZ8naWs/0.jpg)](https://www.youtube.com/watch?v=PH4HtZ8naWs)

Microservices YouTube Einführung

---

Einer der grössten Anwendungsfälle und die stärkste treibende Kraft hinter dem Aufstieg von Containern sind Microservices.

Microservices sind ein Weg, Softwaresysteme so zu entwickeln und zu kombinieren, dass sie aus kleinen, unabhängigen Komponenten bestehen, die untereinander über das Netz interagieren. Das steht im Gegensatz zum klassischen, monolithischen Weg der Softwareentwicklung, bei dem es ein einzelnes, grosses Programm gibt.

Wenn solch ein Monolith dann skaliert werden muss, kann man sich meist nur dazu entscheiden, vertikal zu skalieren (scale up), zusätzliche Anforderungen werden in Form von mehr RAM und mehr Rechenleistung bereitgestellt. Microservices sind dagegen so entworfen, dass sie horizontal skaliert werden können (scale out), indem zusätzliche Anforderungen durch mehrere Rechner verarbeitet werden, auf die die Last verteilt werden kann.

In einer Microservices-Architektur ist es möglich, nur die Ressourcen zu skalieren, die für einen bestimmten Service benötigt werden, und sich damit auf die Flaschenhälse des Systems zu beschränken. In einem Monolith wird alles oder gar nichts skaliert, was zu verschwendeten Ressourcen führt.
 
**Beispiele**

* [Beispiele zum Kurs Microservices-Grundlagen («MISEGR»)](https://github.com/mc-b/misegr)
* [Frontend Microservices (Edge Side Include ESI)](https://github.com/mc-b/misegr/tree/master/ewolff#scs-esi-beispiel-frontend)
* [Synchrone Microservices](https://github.com/mc-b/misegr/tree/master/ewolff#microservice-kubernetes-sample)
* [Asynchrone Microservices](https://github.com/mc-b/misegr/tree/master/ewolff#microservice-kafka-sample)


### 701.2 Standard Components and Platforms for Software
*** 

> [⇧ **Nach oben**](#topics)

**Weight**: 2 + 6 Bonuspunkte für die Kombination des Microservices, aus Topic 701.1, mit einer NoSQL Datenbank 

**Description**: Candidates should understand services offered by common cloud platforms. They should be able to include these services in their application architectures and deployment toolchains and understand the required service configurations. OpenStack service components are used as a reference implementation.

Key Knowledge Areas:
* Features and concepts of object storage
* Features and concepts of relational and NoSQL databases
* Features and concepts of message brokers and message queues
* Features and concepts of big data services
* Features and concepts of application runtimes / PaaS
* Features and concepts of content delivery networks

The following is a partial list of the used files, terms and utilities:
* [OpenStack](https://www.openstack.org/software/) Swift
* [OpenStack](https://www.openstack.org/software/) Trove
* [OpenStack](https://www.openstack.org/software/) Zaqar
* [CloudFoundry](https://www.cloudfoundry.org/)
* [OpenShift](https://openshift.io/)

**Unterlagen**

NoSQL Datenbanken
* [Key / Value Stores](https://github.com/mc-b/duk/tree/master/bigdata/redis)
* [Document Stores](https://github.com/mc-b/duk/tree/master/bigdata/mongodb)
* [Graphen Datenbanken](https://github.com/mc-b/duk/tree/master/bigdata/neo4j)
* [Column Family Stores](https://github.com/mc-b/duk/tree/master/bigdata/cassandra)

Big Data
* [Grundlagen](https://github.com/mc-b/bigdata/blob/master/intro/01-Einleitung.md)
* [Charakteristika](https://github.com/mc-b/bigdata/blob/master/intro/02-Charakteristika.md)
* [Datenquellen](https://github.com/mc-b/bigdata/blob/master/intro/20-Datenquellen.md)

Message Brokers und Message Queues
* [Kafka](https://github.com/mc-b/duk/tree/master/kafka)
* [Spark](https://github.com/mc-b/bigdata/tree/master/spark)

Apache WebServer / CGI-BIN / Shellscript
* Beispiel wie mit der CGI Funktionalität eines Web Servers ein ShellScript aufgerufen werden kann.  
* [Docker Image mit Apache Web Server und REST Umgebung](https://github.com/mc-b/IoTKitV2/tree/master/LAM) - siehe rest und restsql Scripts
* Bei den Beispielen ist die IP-Adresse `192.168.55.101` durch die IP-Adresse und Port vom Kubernetes Master zu ersetzen, z.B. `192.168.1.15:32760`
* Eine YAML Datei zum Starten eines vorgefertigten LAM (Linux/Apache/MySQL + REST) Containers befindet sich in [Apache / CGI-BIN / Bash](https://github.com/mc-b/duk/tree/master/iot#apache--cgi-bin--bash). Dieser Container hat steuert auf `http://xx/rest/cgi-bin` statt `http://xx/cgi-bin`.
    
### 701.3 Source Code Management 
*** 

> [⇧ **Nach oben**](#topics)

**Weight**: 5

**Description**: Candidates should be able to use Git to manage and share source code. This includes creating and contributing to a repository as well as the usage of tags, branches and remote repositories. Furthermore, the candidate should be able to merge files and resolve merging conflicts.

Key Knowledge Areas:
* Understand Git concepts and repository structure
* Manage files within a Git repository
* Manage branches and tags
* Work with remote repositories and branches as well as submodules
* Merge files and branches
* Awareness of SVN and CVS, including concepts of centralized and distributed SCM solutions

The following is a partial list of the used files, terms and utilities:
* git
* .gitignore

**Unterlagen**
* [Git Buch](https://git-scm.com/book/de/v2)
* [Gut Buch (Alternative](http://gitbu.ch/pr01.html)
* [GitHub Account](https://github.com/mc-b/M300/tree/master/10-Toolumgebung#-01---github-account)
* [Git Client](https://github.com/mc-b/M300/tree/master/10-Toolumgebung#--02---git-client)

### 701.4 Continuous Integration and Continuous Delivery 
*** 

> [⇧ **Nach oben**](#topics)

**Weight**: 5 + 5 Bonuspunkte für Aussetzen eines eigenes Projektes (Microservice) und dessen CI/CD mittels Jenkins. 

**Description**: Candidates should understand the principles and components of a continuous integration and continuous delivery pipeline. Candidates should be able to implement a CI/CD pipeline using Jenkins, including triggering the CI/CD pipeline, running unit, integration and acceptance tests, packaging software and handling the deployment of tested software artifacts. This objective covers the feature set of Jenkins version 2.0 or later.

Key Knowledge Areas:
* Understand the concepts of Continuous Integration and Continuous Delivery
* Understand the components of a CI/CD pipeline, including builds, unit, integration and acceptance tests, artifact management, delivery and deployment
* Understand deployment best practices
* Understand the architecture and features of Jenkins, including Jenkins Plugins, Jenkins API, notifications and distributed builds
* Define and run jobs in Jenkins, including parameter handling
* Fingerprinting, artifacts and artifact repositories
* Understand how Jenkins models continuous delivery pipelines and implement a declarative continuous delivery pipeline in Jenkins
* Awareness of possible authentication and authorization models
* Understanding of the Pipeline Plugin
* Understand the features of important Jenkins modules such as Copy Artifact Plugin, Fingerprint Plugin, Docker Pipeline, Docker Build and Publish plugin, Git Plugin, Credentials Plugin
* Awareness of Artifactory and Nexus

The following is a partial list of the used files, terms and utilities:
* Step, Node, Stage
* Jenkins SDL
* Jenkinsfile
* Declarative Pipeline
* Blue-green and canary deployment

**Unterlagen**

* [Dokumentation aus Modul M300](https://github.com/mc-b/M300/tree/master/35-Sicherheit#-03---kontinuierliche-integration)
* [Sammlung von DevOps Tools aus dem Kurs Docker und Kubernetes](https://github.com/mc-b/duk/tree/master/devops)
* [Aufbau einer CI/CD Pipeline mit Docker/Kubernetes vom Digicomp DevDay](https://github.com/mc-b/devday#aufbau-einer-continous-integration--delivery-pipeline-mit-dockerkubernetes)
* [Einfaches Projekt mit Jenkinsfile](https://github.com/mc-b/simple-java-maven-app)
* [Microservices Projekt mit Erstellung von Containern](https://github.com/mc-b/SCS-ESI)

## Topic 702: Container Management

### 702.1 Container Usage 
*** 

> [⇧ **Nach oben**](#topics)

**Weight**: 7 (nur wer das Modul M300 nicht besucht hat + 7 Bonuspunkte). Es wird ein Beschrieb Linux Technologien und Container erwartet.

**Description**: Candidates should be able to build, share and operate Docker containers. This includes creating Dockerfiles, using a Docker registry, creating and interacting with containers as well as connecting containers to networks and storage volumes. This objective covers the feature set of Docker version 17.06 or later.

Key Knowledge Areas:
* Understand the Docker architecture
* Use existing Docker images from a Docker registry
* Create Dockerfiles and build images from Dockerfiles
* Upload images to a Docker registry
* Operate and access Docker containers
* Connect container to Docker networks
* Use Docker volumes for shared and persistent container storage

The following is a partial list of the used files, terms and utilities:
* docker
* Dockerfile
* .dockerignore

**Unterlagen**
* [Docker Homepage](https://www.docker.com/)
* [The Missing Introduction To Containerization](https://medium.com/devopslinks/the-missing-introduction-to-containerization-de1fbb73efc5)
* [Linux Namespaces](http://man7.org/linux/man-pages/man7/namespaces.7.html)
* [A Tutorial for Isolating Your System with Linux Namespaces](https://www.toptal.com/linux/separation-anxiety-isolating-your-system-with-linux-namespaces)
* [unshare](http://manpages.ubuntu.com/manpages/bionic/man1/unshare.1.html)
* [Union FS](https://de.wikipedia.org/wiki/UnionFS)
* [containerd](https://containerd.io/)
* [Open Container Initiative](https://www.opencontainers.org/) und [runc](https://github.com/opencontainers/runc)
* [Container aus dem Modul M300](https://github.com/mc-b/M300/blob/master/30-Container)
* [Container Sicherheit aus dem Modul M300](https://github.com/mc-b/M300/blob/master/35-Sicherheit)

#### Container - Linux Native Variante

Um das Verhalten von Container manuell auf Linux zu Erzeugen holen wir zuerst eine Linux Distribution und entpacken diese in einem Verzeichnis `ubuntu`.

    wget https://github.com/tianon/docker-brew-ubuntu-core/raw/010bf9649b1d10e2c34b159a9a9b338d0fdd4939/xenial/ubuntu-xenial-core-cloudimg-amd64-root.tar.gz -O ubuntu.tgz
    mkdir ubuntu
    cd ubuntu
    tar xzf ../ubuntu.tgz
    
Anschliessend verwenden wir den Befehl `unshare` um in den Namespaces des aktuellen Prozesses zu wechseln.

    sudo unshare -n  -p --fork  --mount-proc /bin/bash
    
Nun sollte nur noch ein `localhost` Netzwerkadapter und keine Prozesse ausser ab dem aktuellen abwärts sichtbar sein.    
    
    ping google.com
    ifconfig -a
    pstree -n -p
    
Das Filesystem können wir allerdings noch sehen. Das unterbinden wir mit dem Befehl `chroot`

    chroot .
    
Nun laufen wir in einer sogenannten **Sandbox** oder halt in einem **Container**. Beenden bzw. Rückkehr auf Host OS mittels 2 mal `exit`.

Ausprobieren durch die Anzeige der HOME Verzeichnis

    ls -l /home
    
Auch sind eine Reihe von Befehlen, aus Sicherheitsgründen, nicht mehr vorhanden, z.B.:

    sudo -i
    ifconfig -a
    
#### Container - Docker Variante

Docker ist ein Produkt welche diese Funktionalität mittels des Kommandozeilenprogrammes `docker` zur Verfügung stellt.

    docker run -it ubuntu /bin/bash
    
Es wird das Container Image `ubuntu` von [https://hub.docker.com](https://hub.docker.com) geholt und als Container gestartet. Beenden bzw. mittels `exit`.

#### Container - Kubernetes Variante

Kubernetes erweitert die Docker Funktionalität um die Möglichkeit mehrere Containers Hosts zu einem Cluster zusammenzustellen.

Haben wir z.B. ein Cluster mit 3 Container Hosts, erzeugt der folgende Befehle 20 Container, mit dem Apache Web Server, und verteilt diese auf die drei Hosts.

    kubectl run apache --replicas=20 --expose=true --image=httpd --port=80 
    
Das Resultat können wir uns wie folgt anschauen:

    kubectl get pods --selector=run=apache -o wide 

### 702.2 Container Deployment and Orchestration 
*** 

> [⇧ **Nach oben**](#topics)

**Weight**: 5

**Description**: Candidates should be able to run and manage multiple containers that work together to provide a service. This includes the orchestration of Docker containers using Docker Compose in conjunction with an existing Docker Swarm cluster as well as using an existing Kubernetes cluster. This objective covers the feature sets of Docker Compose version 1.14 or later, Docker Swarm included in Docker 17.06 or later and Kubernetes 1.6 or later.

Key Knowledge Areas:
* ~~Understand the application model of Docker Compose~~
* ~~Create and run Docker Compose Files (version 3 or later)~~
* ~~Understand the architecture and functionality of Docker Swarm mode~~
* ~~Run containers in a Docker Swarm, including the definition of services, stacks and the usage of secrets~~
* Understand the architecture and application model Kubernetes
* Define and manage a container-based application for Kubernetes, including the definition of Deployments, Services, ReplicaSets and Pods

The following is a partial list of the used files, terms and utilities:
* docker-compose
* docker
* kubectl
 
**Unterlagen**

[![](https://img.youtube.com/vi/A4A7ybtQujA/0.jpg)](https://www.youtube.com/watch?v=A4A7ybtQujA)

Kubernetes Core primitives und Running Microservices

---

* [Kubernetes Homepage](https://kubernetes.io/) 
* [Container aus dem Modul M300](https://github.com/mc-b/M300/blob/master/30-Container)
* [Container Sicherheit aus dem Modul M300](https://github.com/mc-b/M300/blob/master/35-Sicherheit)
* [Kubernetes aus dem Modul M300](https://github.com/mc-b/M300/tree/master/40-Kubernetes)

    
#### osTicket Applikation Deployment

[osTicket](http://osticket.com/) ist ein Open-Source-Support-Ticket-System. 

Es leitet Anfragen, die per E-Mail, Webformularen und Telefonanrufen erstellt wurden, nahtlos in eine einfache, benutzerfreundliche webbasierte Kunden-Support-Plattform für mehrere Benutzer um.

osTicket besteht aus einem Frontend welches die Daten in einer Datenbank, vorzugsweise MySQL, speichert.

osTicket kann wie folgt gestartet werden:

    kubectl apply -f duk/osticket/
    
Es wird das osTicket Frontend und MySQL gestartet. Jeder Container bekommt eine eindeutige IP und einen DNS Namen (mittels Service). Über diesen DNS Namen finden sich die Container.   

    kubectl get pods,services --selector=app=osticket -o wide
    
Um osTicket zu Testen brauchen wir den weitergeleiteten Port. Dieser kann wie folgt ermittelt werden:

    kubectl config view -o=jsonpath='{ .clusters[0].cluster.server }' | sed -e 's/https:/http:/' -e "s/6443/$(kubectl get svc osticket -o=jsonpath='{ .spec.ports[0].nodePort }')/"

### Rolling Update

Kubernetes  unterstützt das Aktualisieren von Images auf eine neue Version mithilfe eines fortlaufenden Aktualisierungs-mechanismus

Zuerst brauchen wir einen Container mit verschiedenen Versionen (Tags). 

    kubectl apply -f https://raw.githubusercontent.com/mc-b/misegr/master/bpmn/bpmn-frontend.yaml 
  
Um das Frontend anzuschauen starten wir den Browser mit [https://localhost:30443/frontend/index.html](https://localhost:30443/frontend/index.html).

Nun ändern wir die Version von `latest` auf Version 1.0.

    kubectl set image deployment/bpmn-frontend bpmn-frontend=misegr/bpmn-frontend:V1.0

Nach dem refereshen des Browser sollte `V1.0` über eingeblendet sein.

Was beim Rolling Update passiert können wir uns wie folgt anzeigen lassen:

    kubectl describe deployment/bpmn-frontend

## 702.3 Container Infrastructure 
***

> [⇧ **Nach oben**](#topics)

**Weight**: 4

**Description**: Candidates should be able to set up a runtime environment for containers. This includes running containers on a local workstation as well as setting up a dedicated container host. Furthermore, candidates should be aware of other container infrastructures, storage, networking and container specific security aspects. This objective covers the feature set of Docker version 17.06 or later and Docker Machine 0.12 or later.

Key Knowledge Areas:
* ~~Use Docker Machine to setup a Docker host~~
* ~~Understand Docker networking concepts, including overlay networks~~
* ~~Create and manage Docker networks~~
* ~~Understand Docker storage concepts~~
* ~~Create and manage Docker volumes~~
* Awareness of Flocker and flannel
* Understand the concepts of service discovery
* Basic feature knowledge of CoreOS Container Linux, rkt and etcd
* Understand security risks of container virtualization and container images and how to mitigate them

The following is a partial list of the used files, terms and utilities:
* docker-machine

**Unterlagen**
* [Aufsetzen einer Kubernetes Umgebung](https://github.com/mc-b/duk#beispiele-zum-kurs-docker-und-kubernetes--%C3%BCbersicht-und-einsatz-)
* [Kubernetes Homepage](https://kubernetes.io/) 
* [Kubernetes aus dem Modul M300](https://github.com/mc-b/M300/tree/master/40-Kubernetes)

## Topic 703: Machine Deployment

### 703.1 Virtual Machine Deployment 
***

> [⇧ **Nach oben**](#topics)

**Weight**: 4 

**Description**: Candidates should be able to automate the deployment of a virtual machine with an operating system and a specific set of configuration files and software.

Key Knowledge Areas:
* Understand Vagrant architecture and concepts, including storage and networking
* Retrieve and use boxes from Atlas
* Create and run Vagrantfiles
* Access Vagrant virtual machines
* Share and synchronize folder between a Vagrant virtual machine and the host system
* Understand Vagrant provisioning, including File, Shell, Ansible and Docker
* Understand multi-machine setup

The following is a partial list of the used files, terms and utilities:
* vagrant
* Vagrantfile
 
**Unterlagen**
* [Infrastruktur-Automatisierung aus dem Modul M300, Kapitel 01 - 03](https://github.com/mc-b/M300/tree/master/20-Infrastruktur)
* [Infrastruktur-Sicherheit aus dem Modul M300](https://github.com/mc-b/M300/tree/master/25-Sicherheit)
* [Vagrant Homepage](https://www.vagrantup.com/)
* [Vagrant Boxes (Atlas)](https://app.vagrantup.com/boxes/search)

### 703.2 Cloud Deployment
***

> [⇧ **Nach oben**](#topics)

**Weight**: 2

**Description**: Candidates should be able to configure IaaS cloud instances and adjust them to match their available hardware resources, specifically, disk space and volumes. Additinally, candidates should be able to configure instances to allow secure SSH logins and prepare the instances to be ready for a configuration management tool such as Ansible.

Key Knowledge Areas:
* Understanding the features and concepts of cloud-init, including user-data and initializing and configuring cloud-init
* Use cloud-init to create, resize and mount file systems, configure user accounts, including login credentials such as SSH keys and install software packages from the distribution’s repository
* Understand the features and implications of IaaS clouds and virtualization for a computing instance, such as snapshotting, pausing, cloning and resource limits.

**Unterlagen**
* [Azure Cloud IaaS](https://azure.microsoft.com/de-de/overview/what-is-azure/iaas/)
* [AWS Cloud](https://aws.amazon.com/de/types-of-cloud-computing/)
* [Infrastruktur-Automatisierung aus dem Modul M300, Kapitel 05 AWS Cloud](https://github.com/mc-b/M300/tree/master/20-Infrastruktur#-05---aws-cloud)

### 703.3 System Image Creation
***

> [⇧ **Nach oben**](#topics)

**Weight**: 2

**Description**: Candidates should be able to create images for containers, virtual machines and IaaS cloud instances.

Key Knowledge Areas:
* Understand the functionality and features of Packer
* Create and maintain template files
* Build images from template files using different builders

The following is a partial list of the used files, terms and utilities:
* packer

**Unterlagen**
* [Infrastruktur-Automatisierung aus dem Modul M300, Kapitel 04 Packer](https://github.com/mc-b/M300/tree/master/20-Infrastruktur#-04---packer)

## Topic 704: Configuration Management

### 704.1 Ansible 
***

> [⇧ **Nach oben**](#topics)

**Weight**: 8

**Description**: Candidates should be able to use Ansible to ensure a target server is in a specific state regarding its configuration and installed software. This objective covers the feature set of Ansible version 2.2 or later.

Key Knowledge Areas:
* Understand the principles of automated system configuration and software installation
* Create and maintain inventory files
* Understand how Ansible interacts with remote systems
* Manage SSH login credentials for Ansible, including using unprivileged login accounts
* Create, maintain and run Ansible playbooks, including tasks, handlers, conditionals, loops and registers
* Set and use variables
* Maintain secrets using Ansible vaults
* Write Jinja2 templates, including using common filters, loops and conditionals
* Understand and use Ansible roles and install Ansible roles from Ansible Galaxy
* Understand and use important Ansible tasks, including file, copy, template, ini_file, lineinfile, patch, replace, user, group, command, shell, service, systemd, cron, apt, debconf, yum, git, and debug
* Awareness of dynamic inventory
* Awareness of Ansibles features for non-Linux systems
* Awareness of Ansible containers

The following is a partial list of the used files, terms and utilities:
* ansible.cfg
* ansible-playbook
* ansible-vault
* ansible-galaxy
* ansible-doc

**Unterlagen**

* [ansible Homepage](https://www.ansible.com/) 

### 704.2 Other Configuration Management Tools 
***

> [⇧ **Nach oben**](#topics)

**Weight**: 2

**Description**: Candidates should understand the main features and principles of important configuration management tools other than Ansible.

Key Knowledge Areas:
* Basic feature and architecture knowledge of Puppet.
* Basic feature and architecture knowledge of Chef.

The following is a partial list of the used files, terms and utilities:
* Manifest, Class, Recipe, Cookbook
* puppet
* chef
* chef-solo
* chef-client
* chef-server-ctl
* knife

**Unterlagen**

* [puppet Homepage](https://puppet.com/de)
* [chef Homepage](https://www.chef.io/)

## Topic 705: Service Operations

### 705.1 IT Operations and Monitoring 
***

> [⇧ **Nach oben**](#topics)

**Weight**: 4

**Description**: Candidates should understand how IT infrastructure is involved in delivering a service. This includes knowledge about the major goals of IT operations, understanding functional and nonfunctional properties of an IT services and ways to monitor and measure them using Prometheus. Furthermore candidates should understand major security risks in IT infrastructure. This objective covers the feature set of Prometheus 1.7 or later.

Key Knowledge Areas:
* Understand goals of IT operations and service provisioning, including nonfunctional properties such as availability, latency, responsiveness
* Understand and identify metrics and indicators to monitor and measure the technical functionality of a service
* Understand and identify metrics and indicators to monitor and measure the logical functionality of a service
* Understand the architecture of Prometheus, including Exporters, Pushgateway, Alertmanager and Grafana
* Monitor containers and microservices using Prometheus
* Understand the principles of IT attacks against IT infrastructure
* Understand the principles of the most important ways to protect IT infrastructure
* Understand core IT infrastructure components and their the role in deployment

The following is a partial list of the used files, terms and utilities:
* Prometheus, Node exporter, Pushgateway, Altermanager, Grafana
* Service exploits, brute force attacks, and denial of service attacks
* Security updates, packet filtering and application gateways
* Virtualization hosts, DNS and load balancers

**Unterlagen**

* [Kubernetes monitoring with Prometheus in 15 minutes](https://itnext.io/kubernetes-monitoring-with-prometheus-in-15-minutes-8e54d1de2e13)

### 705.2 Log Management and Analysis
***

> [⇧ **Nach oben**](#topics)

**Weight**: 4

**Description**: Candidates should understand the role of log files in operations and troubleshooting. They should be able to set up centralized logging infrastructure based on Logstash to collect and normalize log data. Furthermore, candidates should understand how Elasticsearch and Kibana help to store and access log data.

Key Knowledge Areas:
* Understand how application and system logging works
* Understand the architecture and functionality of Logstash, including the lifecycle of a log message and Logstash plugins
* Understand the architecture and functionality of Elasticsearch and Kibana in the context of log data management (Elastic Stack)
* Configure Logstash to collect, normalize, transform and store log data
* Configure syslog and Filebeat to send log data to Logstash
* Configure Logstash to send email alerts
* Understand application support for log management

The following is a partial list of the used files, terms and utilities:
* logstash
* input, filter, output
* grok filter
* Log files, metrics
* syslog.conf
* /etc/logstash/logstash.yml
* /etc/filebeat/filebeat.yml

**Unterlagen**

* [Logging](https://github.com/w901-fr19-mi/E010/blob/master/md/10-Linux-System/19-Logging.md)
* [Docker Logging](https://docs.docker.com/config/containers/logging/configure/)
* [Kubernetes Logging](https://kubernetes.io/docs/concepts/cluster-administration/logging/)

## Bonusmaterial

> [⇧ **Nach oben**](#topics)

* [CNCF Cloud Native Trail Map um ihre Cloud-native Reise zu beginnen](https://github.com/cncf/trailmap)
* [CNCF Cloud native Landkarte](https://landscape.cncf.io/)
* [50 Best Kubernetes Architecture Tutorials](https://securityboulevard.com/2019/04/50-best-kubernetes-architecture-tutorials/)
* [Container Design Patterns for Kubernetes - Part 1](https://www.weave.works/blog/container-design-patterns-for-kubernetes/)
* [Praxiserfahrung DevOps – DevOps was?](https://www.digicomp.ch/blog/2019/04/25/praxiserfahrung-devops-devops-was)

