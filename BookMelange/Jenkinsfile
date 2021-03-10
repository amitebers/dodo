pipeline {

   agent any

   stages {

      stage('Build') {

         steps {

            git 'https://github.com/<your-username>/simple-app.git'

            bat "mvn -Dmaven.test.failure.ignore=true clean package"

         }


         post {

            success {

               

               archiveArtifacts 'target/*.jar'

            }

         }

      }

   }

}