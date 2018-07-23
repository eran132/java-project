pipeline {
    agent any
    
    stages {
        stage ('build') {
            steps{
                sh 'ant -f build.xml -v'
		        sh 'echo hello  yes ok world'
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'dist/*.jar', fingerprint: true
        }
    }
}
