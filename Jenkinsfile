pipeline {
    agent any
    options {
        timeout(time:1, unit:'HOURS')
        retry(3)
    }
    input {
        message "please input sth."
        ok "Start"
        submitter 'One,Two',
        parameters {
            string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
            text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
            booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
            choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
            password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
            file(name: "FILE", description: "Choose a file to upload")
        }
    }
    environment {
        TT = 'this is a test environment'
    }
    stages {
        stage('Source') {
            environment {
                AN_ACCESS_KEY = credentials('my-prefined-secret-text')
            }
            steps {
                echo 'Hello World'
                echo "${params.PERSON}"
                echo "${params.BIOGRAPHY}"
                echo "${params.TOGGLE}"
                echo "${params.CHOICE}"
                echo "${params.PASSWORD}"
                echo "${params.FILE}"
            }
        }
    }
}