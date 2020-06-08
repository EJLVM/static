pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-east-1', credentials:'static') {
                    s3upload(
                        pathStyleAccessEnabled: true,
                        payloadSigningEnabled: true,
                        file:'index.html',
                        bucket:'udy-jenkins-s3'
                    )
                sh 'echo "Hello World!"'
                sh '''
                    echo "Multiline shell steps work too"
                    ls -lah
                '''
            }
        }
    }
}