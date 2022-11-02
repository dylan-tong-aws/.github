---
name: 💭 ML Workload Extensibility
about: a connector framework for accelerating ML workload integrations
title: '[ML Workload Extensibility]'
labels: ML Workload Extensibility
assignees: ''
---
## What/Why
### What are you proposing?

This is a proposal for a connector framework that will enables contributors to integrate external systems to serve ML workloads. This framework will introduce integrators to a new integration pardigm that will require much less effort than building and maintaining custom plugins. The first phase of this framework will be designed to enable integrations with ML model serving technologies like Amazon SageMaker hosting services, NVIDIA Triton, Tensorflow Serving and Torch Serve.

### What users have asked for this feature?

Users have provided feedback in our Github proposal (https://github.com/opensearch-project/ml-commons/issues/302) for Deep Learning support.  We have received requests from users for an integration with Amazon SageMaker hosting. A large retailer has also provided us feedback that it is hard to integrate SageMaker models with OpenSearch.

Many data platforms like Amazon Aurora, Amazon Athena, Databricks, Amazon Redshift, Snowflake, Exasol and Teradata support integrations with models hosted on ML platform providers. OpenSearch’s user base also overlaps with users of various ML server technology providers, so we have an opportunity to help our users get more value from their ML technology investments.

### What problems are you trying to solve?

1. *Innovation velocity:* there are so many mature and rapidly evolving model serving technologies. We want to let users select the best technology available to them and benefit from ML capabilities that aren’t natively available on OpenSearch.
2. *Ease of adoption:* many users have already adopted or built their own ML platform. We want to let those users leverage their existing investments and approved technologies.
3. *Limited extensibility:* we do not have an easy way for partners and community contributors to integrate ML technology with OpenSearch. As an open and community-driven platform, it’s important for us to empower contributors to co-innovate and drive joint-GTM motions.

### What is the developer experience going to be?

Stay tune.

#### Are there any security considerations? 
_Describe if the feature has any security considerations or impact. What is the security model of the new APIs? Features should be integrated into the OpenSearch security suite and so if they are not, we should highlight the reasons here._

The framework will be built around our existing APIs in ml-commons and it won't change the existing security models. A connector will manage communication between OpenSearch and an external system's APIs, and it will enforce certain security standards such the API authentication method.

We will provide more details as we near launch and design it around feedback from potential integrators.

#### Are there any breaking changes to the API

No

### What is the user experience going to be?

Initially, this framework will enable integrations with model serving technologies and serve as an alternative to the ML Node for inference workloads. It doesn't change the UX of the features that are powered by OpenSearch's model serving capabilities. For instance, in 2.4, we are releasing support for semantic search which requires ML inference support. The semantic search interfaces will be the same regardless of where the inference workload runs.

#### Are there breaking changes to the User Experience?

No

### Why should it be built? Any reason not to?

We are building this to solve challenges around:

1. *Innovation velocity:* there are so many mature and rapidly evolving model serving technologies. We want to let users select the best technology available to them and benefit from ML capabilities that aren’t natively available on OpenSearch.
2. *Ease of adoption:* many users have already adopted or built their own ML platform. We want to let those users leverage their existing investments and approved technologies.
3. *Limited extensibility:* we do not have an easy way for partners and community contributors to integrate ML technology with OpenSearch. As an open and community-driven platform, it’s important for us to empower contributors to co-innovate and enable joint-GTM motions.

We shouldn’t build this if we feel like we need full control over ML workloads, which doesn't align to our charter as an open and community driven search and analytics suite.


### What will it take to execute?

Stay tune.

### Any remaining open questions?

1. What's your favorite model serving technology? Would it be valuable to provide a distribution that packages the software with an OpenSearch distribution to simplify deployments?
