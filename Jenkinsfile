
pipeline {
    agent any
    tools {
	    maven 'maven-jenkins'
    }
    stages {
        stage('MAVEN BUILD'){
            steps{
                 sh 'mvn clean package -Dmaven.test.skip=true'
            }
        }
        stage('TEST'){
            steps {
                sh 'mvn test'
            }
        }
    }
    post {
        success { 
            echo "This pipeline is successfull!"
            }
    unsuccessful {
            echo "ISSUE!!!"
            }
    }
}
