pipeline {
    agent any
    import jenkins.model.*
    jenkins = Jenkins.instance
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
            echo "${GITCHANGELOG}"
        }
    }
}
