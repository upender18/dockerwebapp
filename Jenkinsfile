node {

    checkout scm

    docker.withRegistry('https://Registry.hub.docker.com', 'dockerHub') {

        def customImage = docker.build("upender18/dockerwebapp")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
