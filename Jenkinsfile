pipeline {
  agent { label 'jenkins-slave-2' }
 
  stages {
    stage('Checkout') {
      steps {
        git branch: 'aula_16', url: 'https://github.com/bcalvessilva/jenkinspipelinepython.git'
      }
    }
    stage('Run') {
      steps {
	    sh 'cd myapp'
	    sh 'python3.10 -m venv venv'
	    sh '. venv/bin/activate'
	    sh 'pip3.10 install Django'
		sh 'pkill python3.10 || true'
        sh 'nohup python3.10 manage.py runserver 0.0.0.0:8000 &'
      }
    }
  }
}
