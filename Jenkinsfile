pipeline {
     environment {
       ID_DOCKER = "${ID_DOCKER_PARAMS}"
       IMAGE_NAME = "alpinehelloworld"
       IMAGE_TAG = "latest"
       APP_NAME = "ulrich"
       STG_API_ENDPOINT = "http://54.172.98.33:1993/"
       STG_APP_ENDPOINT = "http://54.172.98.33:80/"
       PROD_API_ENDPOINT = "http://54.226.195.48:1993/"
       PROD_APP_ENDPOINT = "http://54.226.195.48:80/"
       INTERNAL_PORT = "5000"
       EXTERNAL_PORT = "${PORT_EXPOSED}"
       CONTAINER_IMAGE = "${ID_DOCKER}/${IMAGE_NAME}:${IMAGE_TAG}"
     }
     agent none
     stages {
         stage('Build image') {
             agent any
             steps {
                script {
                  sh 'echo "toto"'
                }
             }
        }


}
