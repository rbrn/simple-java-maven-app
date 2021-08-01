pipeline {
    agent any
    stages {
        stage("Audit"){
            environment {
               VERSION_SUFFIX = getVersionSuffix()
            }
            steps {
                echo "Building version ${VERSION_SUFFIX}"
                auditTools()
            }
        }
    }
}

String getVersionSuffix() {
    return "1.0.0_RELEASE"
}

void auditTools() {
    sh '''
        git version
        java -version
    '''
}
