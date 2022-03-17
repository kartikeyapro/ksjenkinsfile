pipeline {
    agent any
    tools { 
		maven 'Maven 3.0.5'
    }

    stages {
        stage('Git Clone') {
            steps {
				git credentialsId: 'ks-at-531438626024', url: 'https://git-codecommit.us-east-1.amazonaws.com/v1/repos/KartikeyaSoft_Project'
                  }
				}
		stage('Maven Version') {
            steps {
				sh 'mvn --version'
                  }
				}
		stage('mvn clean') {
            steps {
				sh 'mvn clean'
                  }
				}
		stage('mvn validate') {
            steps {
				sh 'mvn validate'
                  }
				}
		
		stage('Maven Compile') {
            steps {
				sh 'mvn compile'
                  }
				}
		stage('Maven Test') {
            steps {
				sh 'mvn test'
                  }
				}	
		stage('Maven Package') {
            steps {
				sh 'mvn package'
                  }
				}	
		stage('Maven deploy') {
            steps {
				sh 'mvn deploy'
                  }
				}			
          
            }
}


