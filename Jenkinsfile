pipeline {
    agent any
    stages {
        stage('hello AWS') {
            steps {
                   
                
                withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'default_region', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
           
                    // bat 'echo "hello KB">hello.txt'
            // s3Upload acl: 'Private', bucket: 'Relicance_BK', file: 'hello.txt'
            // s3Download bucket: 'Relicance_BK', file: 'downloadedHello.txt', path: 'hello.txt'
            //bat 'cat downloadedHello.txt'
               // bat 'aws s3 mb s3://relicankb --region us-east-1'
                    bat 'aws s3 rb s3://relicankb --region us-east-1'
                
            }
            
                //withAWS(credentials: 'aws-credentials', region: 'us-east-1') {
                //    sh 'echo "hello KB">hello.txt'
                //    s3Upload acl: 'Private', bucket: 'kb-bucket', file: 'hello.txt'
                 //   s3Download bucket: 'kb-bucket', file: 'downloadedHello.txt', path: 'hello.txt'
                  //  sh 'cat downloadedHello.txt'
            }
            }
            }
}
