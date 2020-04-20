node {
    checkout scm

    docker.withRegistry('https://registry.example.com', 'credentials-id') {

        def customImage = docker.build("nsdl/node-web-app:${env.BUILD_ID}")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}

