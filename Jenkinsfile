#!/usr/bin/env groovy
pipeline{
	agent any
	stages {
		stage('Build') {
		environment {
                AN_ACCESS_KEY = credentials('1e33c689-dc86-409e-b5af-048b116cfff8') 
				STACK = "teststack"
            }
		steps {
		echo "This is my cft build one"
		cfnUpdate(stack: "$STACK", file: 'template.yaml')
		}
	}
}
}
