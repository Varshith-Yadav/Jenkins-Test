pipeline{
    agent any
    tools{
        maven  'maven'
        jdk  'jdk'
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
        stage("Delivery"){
            steps{
                script{
                    sh './scripts/deliver.sh'
                }
            }
        }
    }
    
}