pipeline {
  agent { label 'jenkins-slave-pf-2' }
 
  stages {
    stage('Checkout') {
      steps {
	      dir("aula_pf") {
                    git branch: 'main', url: 'https://github.com/cabralBRZ/jenkinspipelinepython-aula_15_2.git'
                }
      }
    }
    stage('Run') {
      steps {
	    dir("aula_pf") {
	    sh 'pkill python3.10 || true'
	    sh 'python3.10 -m venv venv'
	    sh '. venv/bin/activate'
	    sh 'pip3.10 install Django'
	    sh 'pip install djangorestframework'
            sh 'pip install markdown'
            sh 'pip install django-filter'
            sh 'pip install pygments'	      
	    sh 'pip install django-crispy-forms'
	    sh 'pip install django-tables2'
	    sh 'pip install drf-spectacular'
	    sh 'JENKINS_NODE_COOKIE=dontKillMe nohup python3.10 manage.py runserver 0.0.0.0:8000 > output.txt&'
	   }
      }
    }
  }
}
