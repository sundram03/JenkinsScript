pipeline {
    agent any
    environment { 
        name = 'sundram'
    }
    parameters{
        string(name: 'person', defaultValue: '', description: 'who are you?' )
        booleanParam(name: 'isMale', defaultValue: true, description: '' )
        choice(name: 'city', choices:['jaipur', 'muzaffarpur','bangalore'], description: '' )
        
    }
    stages {
            stage('Linux Basic command') {
            steps {
                sh '''
                date
                pwd
                cal 2025
                
                '''
            }
        }
        stage('Enviromnent variable') {
            steps {
                sh 'echo "${BUILD_ID}"'
                sh 'echo "${name}"'
            }
        }
        stage('parameter pass') {
            steps {
                sh 'echo "${person}"'
            }
        }
        
         stage('continue') {
            input {
                message "should be continoue ?"
                ok "yes you should"
            }
            steps {
                sh 'echo "${person}"'
            }
        }
         stage('deploy') {
            steps {
                sh 'echo "${person}"'
            }
        }
        
    }
     post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure { 
            echo 'failure'
        }
        success
        { 
            echo 'sucess'
        }
    }
}
