# Techzone Deployer Cloud Pak Deployer pipelines

This repository contains a set of Tekton pipelines to utilize the Cloud Pak Deployer asset in an IBM Technology Zone `deployer` cluster.

## Prerequisites

An IBM Technology Zone `deployer` cluster is assumed to be configured with an appropriate Red Hat OpenShift version for the solution you wish to deploy, with appropriate sizing.

A `deployer` cluster is configured with the following items:

- ExternalSecrets operator deployed with a ClusterSecretStore configured. The remote ExternalSecrets secret store must include an IBM Entitlement Key.
- Techzone Deployer Tekton tasks deployed ([deploy YAML](https://github.com/cloud-native-toolkit/deployer-tekton-tasks/blob/main/argocd.yaml)).
- OpenShift GitOps configured with [One Touch Provisioning ArgoCD instance](https://github.com/one-touch-provisioning/otp-gitops), and any relevant RBAC rules.
- OpenShift Pipelines operator deployed.
- OpenShift Data Foundation

There is also the option to use your own IBM Entitlement key passed in as the parameter ibm-entitlement-key

## Repository organisation

The top-level folders in this repository are for the current Cloud Pak Deployer's Cloud Pak configurations. In each top-level folder there will be a pipeline and a pipelinerun and they may be organized into different folders for different Cloud Pak versions.

```
.
└── cloud-pak-type/
    ├── pipeline.yaml
    └── pipelinerun.yaml
```

## Deployment Scripts

`oc apply -f cp4d-cloud-pak-deployer-pipeline.yaml` to install the pipeline.

`oc create -f cp4d-cloud-pak-deployer-pipeline-run.yaml` to kick off pipeline with base cp4d configuration by default.
