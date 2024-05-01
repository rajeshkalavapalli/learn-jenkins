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
        timeout(time: 1, unit: 'HOURS') 
        disableConcurrentBuilds()
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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
                
                """
            }
        }

        stage ('params') {
            steps {
                sh """
                echo "Hello ${params.PERSON}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"
                
                echo "Toggle": ${params.TOGGLE}
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


