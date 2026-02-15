pipeline {
     agent any
     stages {
          stage('Source') {
               steps {
                    git branch: 'main',
                        url: 'https://github.com/ladyusa/rectangle'
               }
          }
          stage('Build') {
               steps {
                    sh 'javac shape/*.java'
               }
          }
          stage('Test') {
               steps {
                    sh 'java shape.RectangleTest'
               }
          }
          stage('Deploy') {
               steps {
                    sh 'java shape.RectangleMain'
               }
          }
     }
}
