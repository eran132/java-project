pipeline {
    agent any
    
    options {
        buildDiscarder(logRotator(numToKeepStr: '2', artifactNumTokeepStr: '1'))
    }
    stages {
        stage ('build') {
            steps{
                sh 'ant -f build.xml -v'
		        sh 'echo hello  yes world'
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'dist/*.jar', fingerprint: true
        }
    }
}
