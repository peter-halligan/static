pipeline {
   agent any
   stages {
       stage('Build') {
           steps {
               sh 'echo Hello World'
               sh '''
                  echo "Multiline shell workds too"
                  ls -lah
                  '''
           }
       }
       stage('Upload'){
           steps{
               withAws(region:"us-west-2", credentials:'aws-jenkins-id')) {
                   s3Upload(file:'index.html', bucket:'peter-halligan-udacity.project3', path:'index.html')
               }
           }
       }
   }
}