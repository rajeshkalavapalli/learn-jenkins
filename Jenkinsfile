pipeline{
    agent {
        node {
            label 'AGENT-1'
            
        }
    }
         environment { 
                GREETING = 'hello good morning'
            }    
}
    stages {
       
        stage ('git check out') {
            steps {
                sh """
                echo 'git checkingout....'
                env
                """
            }
        }
        stage ('build') {
            steps {
                echo 'build.......'
            }
        }
        stage ('deploye') {
            steps {
                echo 'deploye.......'
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


