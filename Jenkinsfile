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
   }
}