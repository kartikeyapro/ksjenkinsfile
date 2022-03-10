pipeline {
    agent any
    tools { 
		maven 'maven-3.8.4'
    }

    stages {
        stage('Git Clone') {
            steps {
				git credentialsId: 'git', url: 'https://github.com/kartikeyapro/ks.git'
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


