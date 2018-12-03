pipeline {
    agent any
    stages {
        stage('Stage 1') {
            steps {
                // JENKINSHOME is just a name to help readability
                withEnv(['PATH+JENKINSHOME=/var/lib/jenkins/maven/apache-maven-3.6.0/bin']) {
                    echo "PATH is: $PATH"
                    sh 'mvn --version'
                }
            }
        }
        stage('Stage 2') {
            steps {
                echo 'this is stage 2'
                echo 'wish you were here'
            }
        }
    }
}
