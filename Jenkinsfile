pipeline {
    agent any
    options {
        skipDefaultCheckout true
    }

    stages {
        stage('Hello') {
            steps {
                echo "DEBUG: parameter COMMITID = ${env.COMMITID}"
                checkout([$class: 'GitSCM', branches: [[name: '${env.COMMITID}']], extensions: [[$class: 'GitLFSPull']], userRemoteConfigs: [[url: 'https://github.com/harrychu-git/233653.git']]])
            }
        }
    }
}
