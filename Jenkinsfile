pipeline{
    agent any
    stages{
        stage('build'){
            steps{
                withMaven(maven: 'maven_3_9_2'){
                    sh 'make clean compile'
                }
            }
        }
        stage('test'){
            steps{
                withMaven(maven: 'maven_3_9_2'){
                    sh 'mvn test'
                }
            }
        }
        stage('Deploy'){
            steps{
                withMaven(maven: 'maven_3_9_2'){
                    sh 'mvn deploy'
                }
            }
        }
    }
}
