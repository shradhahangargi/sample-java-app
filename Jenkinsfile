pipeline {
  agent any

  tools {
    maven 'Maven 3.9.6'
    jdk 'JDK 17'
  }

  stages {
    stage('Build') {
      steps {
        sh 'mvn clean compile'
      }
    }

    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('Package') {
      steps {
        sh 'mvn package'
      }
    }
  }

  post {
    success {
      echo '✅ Build Success!'
    }
    failure {
      echo '❌ Build Failed!'
    }
  }
}

