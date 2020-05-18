#!/usr/bin/env groovy
pipeline{
	agent any
	stages {
		stage('Build') {
		environment {
                AWS_ACCESS_KEY_ID     = credentials('jenkins-aws-secret-key-id')
				AWS_SECRET_ACCESS_KEY = credentials('jenkins-aws-secret-access-key') 
				STACK = "teststack"
            }
		steps {
		echo "This is my cft build one"
		echo "$AWS_ACCESS_KEY_ID"
		echo "$AWS_SECRET_ACCESS_KEY"
		cfnUpdate(stack: "$STACK", file: 'template.yaml')
		}
	}
}
}
