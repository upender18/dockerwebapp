node {

    checkout scm

    docker.withRegistry('https://hub.docker.com/repository/docker/upender18/dockerimage', 'dockerHub') {

        def customImage = docker.build("upender18/dockerwebapp")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
