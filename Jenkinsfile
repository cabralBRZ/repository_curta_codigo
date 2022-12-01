pipeline {
  agent any
 
  stages {
    stage('Checkout') {
      steps {
        git branch: 'aula_11', url: 'https://github.com/bcalvessilva/jenkinspipelinepython.git'
      }
    }
    stage('Run') {
      steps {
        sh 'python3 app.py'
      }
    }
  }
}
