pipeline {
    agent any
    parameters {
        gitParameter name: 'BRANCH',
                     type: 'PT_BRANCH',
                     defaultValue: 'main'
    }
    stages {
        stage('Example') {
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
    }
}