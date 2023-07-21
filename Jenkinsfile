pipeline {
    agent any

    stages {
        // stage('Exemple') {
        //     steps {
        //         echo "Runnng ${env.BUILD_ID} on ${env.JENKINS_URL}"
        //     }
        // }
        stage('Clone') {
            steps {
                sh "mvn clean"
                sh "git clone https://github.com/Kameli71/Java_maven_demo.git"
                echo "All files deleted from repertory"
                echo "Clonage ok"
            }
        }
        stage('Build') {
            steps {
                sh "cd /demo"
                sh "mvn install package"
                sh "mvn compile"
                sh "javac main/java/com/example/App.java"
                echo 'Moving to git rep'
                echo 'Building and compilation ok'
            }
        }
        stage('Run') {
            steps {
                sh "mvn test"
                sh "mvn verify"
                sh "java main/java/com/example/App.java"
                echo 'launching project'
            }
        }
    }
}