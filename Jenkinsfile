pipeline {
    agent any
    parameters {
    gitParameter branchFilter: 'origin/(.*)', defaultValue: 'main', name: 'BRANCH', type: 'PT_BRANCH'
  }

    stages {
        stage('Execute') {
            steps {
                git branch: "${params.BRANCH}", url: 'https://github.com/jenkinsci/git-parameter-plugin.git'

                
                echo "$pwd"
                echo "${Branch}"
            }
        }
    }
}