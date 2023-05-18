# deployer-cloud-pak-deployer

Tektoncd pipeline to deploy initial Cloud Pak Deployer setup for IBM TechZone Deployer (experimental)

## Prerequisites

- Openshift Cluster with OpenShift Pipelines 1.8 installed
- OpenShift Pipelines
- OpenShift Data Foundation
- IBM Entitlement key or access to Techzone IBM Secrets Manager

## Tasks

Currently uses modified openshift-client and ibmcloud-secrets-manager-get

## Usage

###

oc apply -f cloud-pak-deployer.yaml to install install tasks and pipeline  
oc create -f cloud-pak-deployer-run.yaml to kick off pipeline
