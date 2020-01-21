pipeline { 
    agent any
    stages {
      stage('Upload to AWS') {
          steps {
            sh 'echo "Hello World"'
            sh '''
                echo "Multiline shell steps works too"
                ls -lsh 
                '''
             withAWS(credentials:'jenkins') {
                s3Upload(file:'index.html', bucket:'uniquebucket11', path:'index.html')

                }
               }
            }
          } 
        }
