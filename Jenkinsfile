pipeline {
    agent any
    tools {
        // Note: this should match with the tool name configured in your jenkins instance (JENKINS_URL/configureTools/)
        maven "maven3"
    }
    stages {
        stage("clone code") {
            steps {
                script {
                    // Let's clone the source
                    git 'https://github.com/AnilDevops23/spring3-mvc-maven-xml-hello-world.git';
                }
            }
        }
        stage("mvn build") {
            steps {
                script {
                    // If you are using Windows then you should use "bat" step
                    // Since unit testing is out of the scope we skip them
                    bat(/${MAVEN_HOME}\bin\mvn -Dmaven.test.failure.ignore clean package/)
                }
            }
        }
    }
}
