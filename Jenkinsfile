#!/usr/bin/env groovy

pipeline {
    agent any

    parameters {
        booleanParam(name: 'IAST', 	defaultValue: params.IAST ?: false,
                description: 'Run a scan using WebInspect Standalone for Interactive Application Security Testing (IAST)')        
       
    }   

    stages {
        stage("Fortify WebInpsect - IAST") {
            steps {
                // Execute PowerShell script for IAST scanning
                powershell label: 'IAST with Fortify WebInspect Standalone and WebInspect Agent', returnStatus: true, script: './powershell/iast_automation.ps1'
            }
        }         
    }
}