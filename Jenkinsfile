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
                          userRemoteConfigs: [[url: 'https://github.com/jenkinsci/git-parameter-plugin.git']]
                        ])
            }
        }

        stage('Code Execution') {
            steps {
                echo "${params.Branch}"
                echo "Main Test"
            }
        }
    }
}