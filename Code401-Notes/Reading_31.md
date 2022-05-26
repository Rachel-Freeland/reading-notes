# Reading Day - 29 --> Django REST Framework & Docker

## Reading 
- [Beginner's Guide to Docker](https://wsvincent.com/beginners-guide-to-docker/)
- [Django for APIs - Library Website](https://djangoforapis.com/library-website-and-api/)

* Docker is a way to isolate and run entire applications.
* Docker is really ***Linux Containers*** which are a type of virtualization.
* Images and containers are 2 fundamental concepts to grasp when it comes to working with Docker.
  * An image is a snapshot in time of what a project ***contains***
  * A container is a running ***instance*** of that image
  * An analogy:
    * A `Dockerfile` is the recipe for a cake
    * An ***image*** is a snapshot of the recipe at that given time
    * A `docker-compose.yml` shows how to make the cake
    * And... the ***container*** is the actual, baked cake
* Docker is a great alternative to VMs
* Containers are stateless.
* Images are made from the commandline alot like you would set-up a directory for any other repo...
  * `mkdir code && cd code`
  * `mkdir python3.7 && cd python3.7`
  * `Dockerfile` is similar to `requirements.txt` or `Pipenv` - it creates a list of requirements needed to build the image.
  * `touch Dockerfile` - Dockerfiles are read from top to bottom. The first instruction should be the `FROM` command.
  * The `FROM` command lets us import a base image... either another Docker image or one we create from scratch.
* Image is built with the `docker image build .` command
  * The build should end with `Successfully built` and the hash id
* Images can be made up of one or more image layers a.k.a. `image layering`. Often, image layering is done for 1 of 2 
  main reasons:
  * Each layer is immutable
  * Performance
    * ORDER MATTERS because docker caches the steps to needed to build to speed up subsequent builds.


### Bookmark & Review
- [Beginner's Guide to Django REST Framework](https://learndjango.com/tutorials/official-django-rest-framework-tutorial-beginners)