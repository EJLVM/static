pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World!"'
                sh '''
                    echo "Multiline shell steps work too"
                    ls -lah
            }
        }
        
        stage('Upload to AWS') {
            steps {
                
                withAWS(credentials:'jenkins-pipeline-aws') {
                    // do something
                    s3Upload(bucket:"ud-jenkins-s3", file:'index.html')
                }
            }
        }
    }
}