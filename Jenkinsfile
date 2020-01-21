pipeline { 
    agent any
    stages {
      stage('Upload to AWS') {
          steps {
            sh 'echo "Hello World"'
            sh '''
                echo "Fuuuuuuuuuuuuuuuuuuuck"
                ls -lsh 
                '''
               
             withCredentials([[ $class: 'AmazonWebServicesCredentialsBinding', credentialsId: 'jenkins', accessKeyVariable: 'AKIAXEBL5HKAFGX6GQ67', secretKeyVariable: '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']]) {
                sh "echo this is ${env.AWS_ACCESS_KEY_ID}"
                sh "echo this is ${env.AWS_SECRET_ACCESS_KEY}"
                s3Upload(file:'index.html', bucket:'uniquebucket11', path:'index.html')
            }

                }
               }
            }
          } 
