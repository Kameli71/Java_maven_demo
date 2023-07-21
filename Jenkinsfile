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
                sh "rm -rf java/"
                sh "git clone https://github.com/Kameli71/java"
                echo "All files deleted from repertory"
                echo "Clonage ok"
            }
        }
        stage('Build') {
            steps {
                sh "cd /java"
                sh "javac Javajenkins.java"
                echo 'Moving to git rep'
                echo 'Building ok'
            }
        }
        stage('Run') {
            steps {
                sh "java Javajenkins.java"
                echo 'launching project'
            }
        }
    }
}