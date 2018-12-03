pipeline {
    agent any
    stages {
        stage('Stage 1') {
            steps {
                // JENKINSHOME is just a name to help readability
                withEnv(['PATH+JENKINSHOME=/var/lib/jenkins/maven/apache-maven-3.6.0/bin']) {
                    echo "PATH is: $PATH"
                    sh 'mvn --version'
                    sh 'mvn package'
                }
            }
        }
        stage('Stage 2') {
            steps {
                withEnv(['PATH+JENKINSHOME=/var/lib/jenkins/maven/apache-maven-3.6.0/bin']) {
                    echo 'this is stage 2'
                    sh 'java -cp target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App' 
                }
            }
        }
    }
}
