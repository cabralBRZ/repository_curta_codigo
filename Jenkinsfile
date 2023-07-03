pipeline {
  agent { label 'mestre' }
 
  stages {
    stage('Checkout') {
      steps {
        git branch: 'aula_15_2', url: 'https://github.com/cabralBRZ/jenkinspipelinepython.git'
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
