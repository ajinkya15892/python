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
            }
        }
        stage('Deployment') {
            steps {
                sh 'python --version >> /tmp/python.txt'
                echo "$BRANCH_NAME_SAFE"
                echo "$BUILD_NUMBER"
                //dir('publish') { deletedir}
            }
post {
echo "feature branch" 
}
        }
    }
}
