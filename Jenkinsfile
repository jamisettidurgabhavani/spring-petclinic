pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''./mvnw sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.projectName=\'Petclinic\' \\
  -Dsonar.host.url=http://52.66.217.162:9000 \\
  -Dsonar.token=sqp_7d6a29c63f29f48d8d5c1f14054aaf35eb381b9c'''
      }
    }

  }
}