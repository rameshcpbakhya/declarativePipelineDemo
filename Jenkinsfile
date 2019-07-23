pipeline {
         agent any
         
         stages {
                 stage('One') {
                 steps {
                     echo 'Hi, this is Ramesh from Academy'
                 }
                 }
                 stage('Two') {
                 steps {
                    input('Do you want to proceed?')
                 }
                 }
                 stage('Three') {
                 when {
                        {
                          branch "master"
                      }
                         
                 }
                 steps {
                       echo "Hello"
                 }
                 }
          }
}
