pipeline{
    agent any
        stages {
        stage('compile') {
            steps {
                withMaven(maven : 'Maven')
                sh 'mvn clean compile'
            }
        }
       
		stage('Test') {
            steps {
                withMaven(maven : 'Maven')
                sh 'mvn test'
            }
        }
      
		stage('deploy') {
            steps {
                withMaven(maven : 'Maven')
                sh 'mvn deploy'
            }
        }

        }
    
}
