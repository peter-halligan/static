pipeline {
   agent any
   stages {
       stage('Lint html') {
           steps {
               sh 'tidy -q -e *.html'
           }
       }
       stage('Upload'){
           steps{
               withAWS(region:"us-west-2", credentials:'aws-jenkins-id') {
                   s3Upload(file:'index.html', bucket:'peter-halligan-udacity-project3', path:'index.html')
               }
           }
       }
   }
}