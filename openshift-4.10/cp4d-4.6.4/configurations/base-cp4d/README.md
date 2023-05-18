# deployer-cp4d

Tektoncd pipeline to deploy base CP4D foundational services and control plane via Cloud Pak Deployer for IBM TechZone Deployer (experimental)

## Prerequisites

- Openshift Cluster with OpenShift Pipelines 1.8 installed
- OpenShift Pipelines
- OpenShift Data Foundation
- IBM Entitlement key or access to Techzone IBM Secrets Manager
- Cloud Pak Deployer initial configuration on Cluster

## Tasks

Currently uses modified openshift-client

## Usage

###

oc apply -f base-cp4d.yaml to install install tasks and pipeline  
oc create -f base-cp4d-run.yaml to kick off pipeline
