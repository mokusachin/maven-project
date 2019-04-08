pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh  'Bmaven clean package'
            }

        post {
            success {
                echo 'now archiving...'
                archiveArtifacts artifacts :'**/target/*.war'
            }

            }
        }
    }
}