pipeline {
    agent any
    stages {
        stage('hello AWS') {
            steps {
            withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AKIAJZBYAC5M64DQUK7A', credentialsId: 'Default_region', secretKeyVariable: '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']]) {
            // bat 'echo "hello KB">hello.txt'
            // s3Upload acl: 'Private', bucket: 'Relicance_BK', file: 'hello.txt'
            // s3Download bucket: 'Relicance_BK', file: 'downloadedHello.txt', path: 'hello.txt'
            //bat 'cat downloadedHello.txt'
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
