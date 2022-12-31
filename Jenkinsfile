pipeline {
  agent { label 'jenkins-slave' }
 
  stages {
    stage('Checkout') {
      steps {
        git branch: 'aula_16', url: 'https://github.com/bcalvessilva/jenkinspipelinepython.git'
      }
    }
    stage('Run') {
      steps {
        sh 'python3 -m pip install -r requirements.txt'
        sh 'python3 manage.py runserver 0.0.0.0:8000 &'
      }
    }
  }
}