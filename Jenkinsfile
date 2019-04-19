pipeline {
     agent any
     stages {
          stage("Compile") {
               steps {
                    sh "echo Compile"
               }
          }
          stage("Unit test") {
               steps {
                    sh "echo Teste"
               }
          }

          stage("Package") {
               steps {
                    sh "unzip www.zip"
               }
          }

          stage("Docker build") {
               steps {
                    sh "docker build --no-cache -t app-test ."
               }
          }

          stage("Deploy") {
               steps {
                     sh "docker run -p 81:80 -e VIRTUAL_HOST=web1.app.local -d app-test"
               }
         }
     }
}
