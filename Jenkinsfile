pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(credentials: 'jenkins-pipeline-aws') {
          s3Upload(bucket: 'ud-jenkins-s3', file: 'index.html')
        }

      }
    }

  }
}