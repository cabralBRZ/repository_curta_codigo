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
		sh 'pkill python3.10 || true'
	    sh 'python3.10 -m venv venv'
	    sh '. venv/bin/activate'
	    sh 'pip3.10 install Django'
	    sh 'pwd'
        sh 'JENKINS_NODE_COOKIE=dontKillMe nohup python3.10 manage.py runserver 0.0.0.0:8000 > output.txt&'
      }
    }
  }
}
