pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                sh '/home/rong/www/software/apache-maven-3.8.6/bin/mvn -B -DskipTests clean package' 
            }
        }
    }
}
