library identifier: 'groovy-common-tools@master',
       retriever: modernSCM([$class: 'GitSCMSource', remote: 'https://github.com/rbrn/groovy-common-tools.git'])

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