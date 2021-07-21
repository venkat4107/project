pipeline {	
    agent any	

    stages {	
        stage('Build') {	
            steps {	
                echo 'Building..'	
                sh 'mvn compile'	
        }	
}	
        stage('Test') {	
            steps {	
                echo 'Testing..'	
                sh 'mvn test'	
            }	
        }	
        stage('Sonar Analysis') {	
            steps {	
                echo 'Sonar Analysis....'
		sh 'mvn test sonar:sonar -Dsonar.host.url=http://52.0.24.151:9000 -Dsonar.login=3771fcb9872427ce0e7e02da1c229596c3a7ec25'
            
	    }	
        }	
    }	
}
