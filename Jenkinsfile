pipeline{
    agent any 
    stages{
        stage("Build"){
            steps{
                echo "========executing Build========"
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========Build executed successfully========"
                }
                failure{
                    echo "========Build execution failed========"
                }
            }
        }
    }
}