pipeline {
  agent { label 'jenkins-slave' }
 
  stages {
    stage('Checkout') {
      steps {
        git branch: 'aula_15', url: 'https://github.com/bcalvessilva/jenkinspipelinepython.git'
      }
    }
    stage('Run') {
      steps {
        sh 'python3 app.py'
      }
    }
  }
}
