pipeline {
    agent any
    environment {
        BRANCH_NAME_SAFE = env.BRANCH_NAME.replace('/','-')
    }
    stages {
        stage('build') {
            steps {
                sh 'python --version >> /tmp/python.txt'
                echo "$BRANCH_NAME_SAFE"
                //dir('publish') { deletedir}
                writeFile file: '/tmp/version.txt', text: 'BRANCH=${BRANCH_NAME_SAFE}'
            }
            post {
                echo "Execution of post stage"
            }
        }
    }
}
