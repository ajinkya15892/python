pipeline {
    agent any
    environment {
        BRANCH_NAME_SAFE = env.BRANCH_NAME.replace('/','-')
    stages {
        stage('build') {
            steps {
                sh 'python --version >> /tmp/python.txt'
                echo "$BRANCH_NAME_SAFE"
                //dir('publish') { deletedir}
            }
        }
    }
}
