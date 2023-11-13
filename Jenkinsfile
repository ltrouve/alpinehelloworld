pipeline {
     environment {
       ID_DOCKER = "${ID_DOCKER_PARAMS}"
       IMAGE_NAME = "alpinehelloworld"
       IMAGE_TAG = "latest"
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
}
