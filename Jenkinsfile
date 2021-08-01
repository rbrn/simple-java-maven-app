pipeline {
    agent any
    stages {
        stage("Audit"){
            steps {
                environment {
                    VERSION_SUFFIX = getVersionSuffix()
                }
                echo "Building version ${VERSION_SUFFIX}"
                sh '''
                    git version
                '''
            }
        }
    }
}

String getVersionSuffix() {
    return "1.0.0_RELEASE"
}
