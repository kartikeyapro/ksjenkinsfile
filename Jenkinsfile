pipeline {
    agent any
    tools { 
		maven 'Maven 3.0.5'
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
		stage('Soanr Scan') {
            steps {
			sh 'mvn sonar:sonar -Dsonar.host.url=http://34.68.243.142:9000 -Dsonar.login=03b2da1f42dac78e5da5b72ccc2a82188249e501'
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


