pipeline { 
    agent any
    stages {
        
      stage('Lint HTML'){
            steps {
                sh 'tidy -q -e *.html'
            
      stage('Upload to AWS') {
          steps {
            sh 'echo "Hello World"'
            sh '''
                echo "Muliline shell scripts works too"
                ls -lah
               
               '''
            withAWS(credentials:'aws-static') {
                s3Upload(file:'index.html', bucket:'udacitybucket11', path:'udacitybucket11/index.html')

    
}
          
                }
               }
            }
          } 
    }
}
