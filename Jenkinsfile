pipeline {
     environment {
       ID_DOCKER = "${ID_DOCKER_PARAMS}"
       IMAGE_NAME = "alpinehelloworld"
       IMAGE_TAG = "latest"
       // PORT_EXPOSED = "80" à paraméter dans le job obligatoirement
       APP_NAME = "ulrich"
       // STG_API_ENDPOINT = "ip10-0-1-3-cc7bafssrdn0fvnms4tg-1993.direct.docker.labs.eazytraining.fr"
       // STG_APP_ENDPOINT = "ip10-0-1-3-cc7bafssrdn0fvnms4tg-80.direct.docker.labs.eazytraining.fr"
       // PROD_API_ENDPOINT = "ip10-0-1-4-cc7bafssrdn0fvnms4tg-1993.direct.docker.labs.eazytraining.fr"
       // PROD_APP_ENDPOINT = "ip10-0-1-4-cc7bafssrdn0fvnms4tg-80.direct.docker.labs.eazytraining.fr"
       STG_API_ENDPOINT = "http://54.172.98.33:1993/"
       STG_APP_ENDPOINT = "http://54.172.98.33:80/"
       PROD_API_ENDPOINT = "http://54.226.195.48:1993/"
       PROD_APP_ENDPOINT = "http://54.226.195.48:80/"       INTERNAL_PORT = "5000"
       EXTERNAL_PORT = "${PORT_EXPOSED}"
       CONTAINER_IMAGE = "${ID_DOCKER}/${IMAGE_NAME}:${IMAGE_TAG}"

     }
     agent none
     stages {
         stage('Build image') {
             agent any
             steps {
                script {
                  sh 'docker build -t ${ID_DOCKER}/$IMAGE_NAME:$IMAGE_TAG .'
                }
             }
        }
     }
