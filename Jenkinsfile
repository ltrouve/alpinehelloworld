pipeline {
     environment {
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
