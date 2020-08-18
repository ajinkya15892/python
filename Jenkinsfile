import jenkins.model.*
pipeline {
    agent any
      stages {
        stage('Example') {
            steps {
                echo 'Hello World'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
            sh label: '', script: 'echo "${GITCHANGELOG}"'
        }
    }
}
