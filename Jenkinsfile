pipeline{
    agent {
        node {
            label 'AGENT-1'
            
        }
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
                echo 'deploye.......'
            }
        }
        
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}


