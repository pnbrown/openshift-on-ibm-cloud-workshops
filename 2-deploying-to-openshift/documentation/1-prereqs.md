# Install Prerequisites

## Access to the IBM Cloud

An [IBM Cloud account](https://cloud.ibm.com/registration) is needed.


We will use the [OpenShift on IBM Cloud](https://cloud.ibm.com/kubernetes/catalog/openshiftcluster) service on IBM Cloud in this hands-on workshop.


## Tools

In order to complete the workshop, you need to install [Docker Desktop](https://docs.docker.com/install/). Docker Desktop is available for Mac and Windows and the Docker Engine can be run natively on Linux.

Several other tools are needed. There are different options to install these tools.

---

### Tools - Option 1: Prebuilt Image with local Code

There is an image on DockerHub with all required tools. In order to use local IDEs and editors to modify code and configuraton files a Docker volume is used. This option  works only for Mac and Linux.

#### Step 1: Run these commands in a terminal

```
$ git clone https://github.com/nheidloff/openshift-on-ibm-cloud-workshops.git
$ cd openshift-on-ibm-cloud-workshops
$ ROOT_FOLDER=$(pwd)
$ docker run -v $ROOT_FOLDER/:/cloud-native-starter -it --rm nheidloff/openshift-workshop-tools:v1
```

#### Step 2: Inside your running Docker image you can access your the local project 

```
root@3f46c41f7303:/usr/local/bin# cd /cloud-native-starter/
root@3f46c41f7303:/cloud-native-starter# ls
root@3f46c41f7303:/cloud-native-starter# ROOT_FOLDER=$(pwd)
```

_Note:_ With the `--rm` option in the docker run command the container is deleted once you exit. This is intended.


### Tools - Option 2: Prebuilt Image with Code in Container

There is an image on DockerHub with all required tools. This option works for Mac, Linux and Windows. To get started as quickly as possible, use this image.

#### Step 1: Run this command in a terminal

```
$ docker run -ti nheidloff/openshift-workshop-tools:v1
```

#### Step 2: After the container has been started, run these commands inside your running Docker image to get the lastest version of the workshop:

```
root@3f46c41f7303:/usr/local/bin# cd /
root@3f46c41f7303:/usr/local/bin# git clone https://github.com/nheidloff/root@3f46c41f7303:/usr/local/bin# openshift-on-ibm-cloud-workshops.git
root@3f46c41f7303:/usr/local/bin# cd openshift-on-ibm-cloud-workshops
root@3f46c41f7303:/usr/local/bin# ROOT_FOLDER=$(pwd)
```

_Note:_ If you using Windows you also need to download or clone the project to your local workstation for the upcoming Docker and Java lab, because you can't use Docker in the 'openshift-workshop-tools' Docker image.


### Tools - Option 3: Install Tools on your Notebook

This approach works only for Mac and Linux (see this [article](https://suedbroecker.net/2019/08/27/definition-of-a-dockerfile-to-use-bash-scripts-on-a-windows-10-machine-for-our-cloud-native-starter-workshop/) for more).

#### Step 1: Install the following tools:

- [oc](https://cloud.ibm.com/docs/containers?topic=containers-cs_cli_install#cli_oc)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
- [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) 
- [curl](https://curl.haxx.se/download.html)
- Optional: [IBM Cloud CLI](https://cloud.ibm.com/docs/home/tools)
- Optional: Editor, for example [Visual Studio Code](https://code.visualstudio.com/) 

#### Step 2: Get the code:

```
$ git clone https://github.com/nheidloff/openshift-on-ibm-cloud-workshops.git
$ cd openshift-on-ibm-cloud-workshops
$ ROOT_FOLDER=$(pwd)
```

