pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/Pratiak/maven-web-app.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Push') {
            steps {
                echo 'This is Push Stage'
            }
        }

        stage('Deploy') {
            steps {
                sh 'sudo  cp /home/ubuntu/maven-web-app/target/maven-web-app.war /opt/tomcat/apache-tomcat-9.0.68/webapps' 

            }
        }

    }

}
