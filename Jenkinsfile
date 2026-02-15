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
                    bat 'javac shape/*.java'
               }
          }
          stage('Test') {
               steps {
                    bat 'java shape.RectangleTest'
               }
          }
          stage('Deploy') {
               steps {
                    bat 'java shape.RectangleMain'
               }
          }
     }
}
