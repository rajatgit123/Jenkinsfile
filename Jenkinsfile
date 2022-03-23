pipeline {
    agent {label 'slave1'}

    stages {
        stage('GIT Checkout') {
            steps {
                echo 'This is Git Checkout Stage'
				git 'https://github.com/adhig93/java_repo1'
            }
        }
		stage('Build Stage') {
            steps {
                echo 'This is Build Stage'
				sh 'mvn clean install'
            }
        }
		stage('PUSH Stage') {
            steps {
                echo 'This is Push Stage'
            }
        }
		stage('Deploy Stage') {
            steps {
                echo 'This is Deploy Stage'
				sh 'sudo cp target/*.war /home/ec2-user/apache-tomcat-9.0.59/webapps'
            }
        }
    }
}
