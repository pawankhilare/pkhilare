#!/usr/bin/env groovy
pipeline{
	agent any
	parameters{
		string(name: 'cftfile', defaultValue: 'template.yml', description: 'cft template')
		string(name: 'stackname', defaultValue: 'test-stack', description: 'cft template')
	}

	stages {
			def update = {
		cfnUpdate(
			file: params.cftfile,
			stack: params.test-stack
			)
			}
		stage('Build') {
		environment { 
                AN_ACCESS_KEY = credentials('1e33c689-dc86-409e-b5af-048b116cfff8') 
            }
		steps {
		echo "This is my cft build one"
		update()
		}
	}
}
}
