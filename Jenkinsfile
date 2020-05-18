#!/usr/bin/env groovy
pipeline{
	agent any
	parameters{
		string(name: 'cftfile', defaultValue: 'template.yml', description: 'cft template')
		string(name: 'Stackname', defaultValue: 'test-stack', description: 'stack name')
	}

	stages {
		stage('Build') {
		steps {
		echo "This is my cft build one"
		cfnDeploy(
			file: params.cftfile,
			stackName: params.Stackname
			)
		}
	}
}
}
