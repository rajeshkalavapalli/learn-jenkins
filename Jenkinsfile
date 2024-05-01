pipeline{
    agent {
        node {
            label 'AGENT-1'
            
        }
}
    environment { 
        GREETING = 'good morning'
    }

    options {
        timeout(time: 1, unit: 'HOURSS') 
        disableConcurrentBuilds()
    }

    stages {
       
        stage ('git check out') {
            steps {
                echo 'git checking out.......'
            }
        }
        stage ('build') {
            steps {
                echo 'build.......'
            }
        }
        stage ('deploye') {
            steps {
                sh """
                    echo 'iam learning jenkins.......'
                    echo '$GREETING'
                    sleep 10 
                """
            }
        }
        
    }
    post { 
        always { 
            echo 'I will always exicute run !'
        }
        failure { 
            echo 'I will always run when failure !'
        }
        success { 
            echo 'I will always run when success !'
        }
    }
}


