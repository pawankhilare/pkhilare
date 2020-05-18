#!/usr/bin/env groovy
pipeline{
	agent any
	parameters{
		string(name: 'StackName', defaultValue: 'test-stack', description: 'cft template')
		string(name: 'CloudFormationTemplate', defaultValue: 'template.yaml', description: 'cft template')
	}

	stages {
		stage('Build') {
		environment { 
                AWS_ACCESS_KEY_ID     = credentials('jenkins-aws-secret-key-id')
				AWS_SECRET_ACCESS_KEY = credentials('jenkins-aws-secret-access-key')
            }
		steps {
		echo "This is my cft build one"
		cfnUpdate(
			stack: params.StackName,
			file: params.CloudFormationTemplate
			)
		}
	}
}
}
