pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                sh '/home/rong/www/software/apache-maven-3.8.6/bin/mvn -B -DskipTests clean package' 
            }
        }
        stage('test') { 
            steps {
                sh '/home/rong/www/software/apache-maven-3.8.6/bin/mvn test' 
            }
            post {
                 always{
                       junit 'target/surefire-reports/*.xml'
                      }
            }
        }
    }
}
