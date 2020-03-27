pipeline {
    agent any
    stages {
        stage('hello AWS') {
            steps {
                   
                
                withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'default_region', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
            bat 'aws s3 mb s3://relicankb --region us-east-1'
                   // bat 'echo "hello KB">hello.txt'
                    // s3Upload acl: 'Private', bucket: 'Relicance_BK', file: 's3file', path: 'D:\\Krishna\\AWS\\jenkins\\workspace\\AWS_Pipeline', text: 'this is s3 file', workingDir: 'AWS_Pipeline'  
                    // s3Download bucket: 'Relicance_BK', file: 'downloadedHello.txt', path: 'hello.txt'
                    //bat 'cat downloadedHello.txt'
               // bat 'aws s3 mb s3://relicankb --region us-east-1'
                    // bat 'aws s3 rb s3://relicankb --region us-east-1'
                    bat '''
                    if [[ -z $(aws s3api head-bucket --bucket relicankb) ]]; then
                    echo "bucket exists"
                    else
                    echo "bucket does not exist or permission is not there to view it."
                    fi
                    '''
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
