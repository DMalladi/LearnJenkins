pipeline {
    agent any
    parameters {
        gitParameter name: 'BRANCH',
                     type: 'PT_BRANCH',
                     defaultValue: 'main'
    }
    stages {
        stage('Git Checkout') {
            steps {
                checkout([$class: 'GitSCM',
                          branches: [[name: "${params.BRANCH}"]],
                          doGenerateSubmoduleConfigurations: false,
                          extensions: [],
                          gitTool: 'Default',
                          submoduleCfg: [],
                          userRemoteConfigs: [[url: 'https://github.com/DMalladi/LearnJenkins.git']]
                        ])
            }
        }

        stage('Code Execution') {
            steps {
                echo "${Branch}"
                echo "Main Test"
            }
        }
    }
}