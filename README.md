# About
This repository contains resources for deploying an AI-powered application featuring an LLM on OpenShift AI and a Retrieval-Augmented Generation (RAG) solution.

It is assumed that an instance of OpenShift AI is already deployed and Nvidia GPUs are already available to be used.

# Steps

## Checking GPUs

After installing OpenShift AI and Nvidia Operator, makes sure that the GPUs can be consumed by OpenShift AI

* Create a new Data Science project: `llm-rag`
* Create a new Workbench and assign an accelerator for it: `test-gpus`
  * For better testing, use `workbenches/test-gpus-1.ipynb`. There is no out-of-the box workbench with all packages installed, hence packages should be installed using pip
  * For lighter testing, use `workbenches/test-gpus-2.ipynb`. For this use a *torch* workbench.

## Configuring Pipelines with an S3 bucket

* From RHOAI, click on **Configure a Pipeline Server** and use an S3 endpoint and bucket for storing Pipeline artifacts.


## Deploy LLM

* Deploy the LLM using a Model from the OpenShift AI Model Catalog

## Chat with LLM

* Import custom workbench: quay.io/rh-aiservices-bu/rhoai-lab-insurance-claim-workbench:3.0.4 
* Use the `workbenches/chat-with-llm`