pipeline {
    agent any()
    stages {
        stage("Audit"){
            steps {
                sh '''
                    git version
                '''
            }
        }
    }
}
