pipeline{
    agent any
    tools{
        maven  'maven'
        JDK  'jdk'
    }

    stages{
        stage("Build"){
            steps{
                script{
                    sh 'mvn -B -DskipTests clean package'
                }
            }
        }
        stage("Test"){
            steps{
                script{
                    sh 'mvn test'
                }
            }
        }
        stage("Deliviry"){
            steps{
                script{
                    sh './scripts/deliver.sh'
                }
            }
        }
    }
    
}