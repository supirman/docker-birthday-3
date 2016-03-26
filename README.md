# Docker Birthday #3 :tada: :birthday: :tada:

> Birthday App Project

### About the Birthday Party :whale2: :boat:
- [Introduction to Docker and Docker Birthday #3 Slides](https://docs.google.com/a/docker.com/presentation/d/1MKQ8KTxeuSYPHp7LjuOy9k8FgzAApH9i-6A1micJa1A/edit?usp=drive_web)
- Video series on setting up Docker on your machine: [Mac](https://www.youtube.com/watch?v=lNkVxDSRo7M), [Windows](https://youtu.be/S7NVloq0EBc) and [Linux](https://www.youtube.com/watch?v=V9AKvZZCWLc)
- [Training materials](#training-materials)
- [Pre-tutorial preparation](#pre-tutorial-preparation)
- [IN-tutorial guidelines](./tutorial.md)

<a href="https://www.docker.com/docker-birthday"><img align="right" src="https://www.docker.com/sites/default/files/illustration-com-container-party.png"></a>



### Training materials:


This year, to celebrate the Docker Project’s 3rd birthday, the Docker community is joining forces with a number of partners in the broader tech and open-source community to host a series of events focused on providing Docker training to beginners during the week of March 21-26.

:warning: **This document prepares you for the birthday party training before you actually attend. If you are already at the training, please go over to the [Tutorial](https://github.com/docker/docker-birthday-3/blob/master/tutorial.md)**

Based on the feedback we’ve received from Docker meetup organizers, we learned that many meetup attendees are new to Docker and we want to make sure that we welcome them warmly into the Docker community. To ensure that these events are inclusive for everyone attending including underrepresented minorities, we’re happy to announce that we have teamed up with the following partners who’re actively contributing to organizing many Docker Birthday celebrations around the world:

- [General Assembly](https://generalassemb.ly/)
- [Microsoft](https://www.microsoft.com/en-us/)
- [Joyent & the NodeJS community](https://www.joyent.com/developers/node)
- [GoBridge] (http://golangbridge.org/)
- [Women Who Go] (http://www.womenwhogo.org/)
- [Ruby Central] (http://rubycentral.org/)
- [Women Who Code] (https://www.womenwhocode.com/)
- [Digital Ocean] (https://www.digitalocean.com/)

Participants in the training will go through the steps involved in running and developing a simple voting app from a fresh computer using the Docker Toolbox. This simple app will include:

![birthday3-app-architecture](./tutorial-images/bd3-architecture.png)

- **A Python webapp**: which lets you vote between several options
- **A Redis queue**: which collects new votes
- **A Java worker**: which consumes votes and stores them in…
- …**A Postgres database**: backed by a Docker volume
- **A Node.js webapp**: which shows the results of the voting in real time

There will be a self-paced beginners’ tutorial for attendees to learn Docker basics as they build and deploy this app locally. Experienced Docker users will serve as mentors to help beginners successfully complete the training.

### Pre-tutorial preparation
At the training, you will need to bring your own computer. Before you go to a birthday party training, there are some steps you should do some preparation to get your work environment ready. Here are the steps:

1. For Linux users, we need you to install [Docker engine] (https://docs.docker.com/engine/installation/) and [Docker compose] (https://docs.docker.com/compose/install/). Make sure you have Docker engine version 1.10.0 or higher and Docker compose version 1.6 or higher by executing 

   ```docker --version && docker-compose version```

1. For PC and Mac users we need you to install [Docker toolbox for Mac and Windows](https://www.docker.com/products/docker-toolbox) and use [Docker Machine] (https://docs.docker.com/machine/get-started/) to create a virtual machine to run your Docker containers. Once your machine is created and you have connected your shell to this new machine, you're ready to run Docker commands on this host.  If you're using Linux you can skip to the next step.
1. If you're new to Docker, pre-pull the docker images for the very basic tutorial

   ```bash
   docker pull hello-world
   docker pull alpine
   docker pull seqvence/static-site
```
1. To run the application and participate in the rest of the training, pre-pull these images

   ```bash
   docker pull mhart/alpine-node
   docker pull python:2.7-alpine
   docker pull manomarks/worker
   docker pull redis:alpine
   docker pull postgres:9.4
   ```
And now you're ready. See you at the birthday party!


