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
             withAWS(credentials:'Username:AKIAXEBL5HKAFGX6GQ67,Password:sHJq/4W3JC73B55FIGjZmlGlaQKqoSLwSegU5yBJ') {
                s3Upload(file:'index.html', bucket:'uniquebucket11', path:'index.html')

                }
               }
            }
          } 
        }
