pipeline {
     agent any
     stages {
         stage('Build') {
             steps {
                 sh 'echo "Hello World"'
                 sh '''
                     echo "Multiline shell steps works too"
                     ls -lah
                 '''
             }
         }
         stage('Lint HTML') {
              steps {
                  sh 'tidy -q -e *.html'
              }
         }
        //  stage('Upload to AWS') {
        //       steps {
        //           withAWS(region:'us-east-2',credentials:'AKIA2P3VEPC5UOKWLUIX/QB0lscPzRJeob/3PwczsBnCgDOgu3ZbZuyuiqyeF') {
        //           sh 'echo "Uploading content with AWS creds"'
        //               s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'static-jenkins-pipeline')
        //           }
        //       }
        //  }
        //  stage('Security Scan') {
        //       steps { 
        //          aquaMicroscanner imageName: 'alpine:latest', notCompleted: 'exit 1', onDisallowed: 'fail'
        //       }
        //  }         
         
     }
}
