# About
This repository contains resources for deploying an AI-powered application featuring an LLM on OpenShift AI and a Retrieval-Augmented Generation (RAG) solution.

It is assumed that an instance of OpenShift AI is already deployed and Nvidia GPUs are already available to be used.

# Steps

## Checking GPUs

After installing OpenShift AI and Nvidia Operator, makes sure that the GPUs can be consumed by OpenShift AI

* Create a new Data Science project: `llm-rag`
* Create a new Workbench and assign an accelerator for it: `test-gpus`


## Deploy LLM

## Chat with LLM

* Use the `workbenches/chat-with-llm`

