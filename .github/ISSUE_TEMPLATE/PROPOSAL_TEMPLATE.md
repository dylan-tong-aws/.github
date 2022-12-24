---
name: 💭 Proposal
about: Suggest an idea for a specific feature you wish to propose to the community for comment
title: '[PROPOSAL]'
labels: proposal
assignees: ''
---
## What/Why
### What are you proposing?

This feature will provide an OpenSearch admins visibility into where ML models are running in an OpenSearch cluster and whether or not they are responsive.

### What problems are you trying to solve?

We're releasing this feature as part of our plan to bring the semantic search features we released in 2.4 from experimental to GA.

Admins are responsible for the stability and performance of the OpenSearch cluster. If semantic search queries are resulting in errors or are degraded in performance, one reason could be because some or all of the supporting ML models aren’t responding to queries. This feature aims to help admins manage semantic search and ML workloads on OpenSearch by providing them visibility into the health of deployed models.

### What is the developer experience going to be?

This feature provides an UI for the [Profile](https://opensearch.org/docs/latest/ml-commons-plugin/api/#profile) API. Developers have the option of creating an alternative UI by building on top of this API.

#### Are there any security considerations? 

The UI will front an enhanced version of the current [Profile](https://opensearch.org/docs/latest/ml-commons-plugin/api/#profile) API. Thus, the user will require permissions to invoke the Profile API in order to use this dashboard. 

We are also working on adding model-level access controls, which will provide another layer of permissions to control what models a user can view.

#### Are there any breaking changes to the API

We are going to enhance the Profile API as part of this feature. Currently, the Profile API only provides visibility into the models that are responding. It does not provide visibility into where the unresponsive models are running. We plan to add this information in the API’s response.

We don't plan to deprecate the Profile API since it is currently under experimental.

### What is the user experience going to be?

This is a mock-up of the UI will provide:

![mock-up](https://github.com/dylan-tong-aws/opensearch-issues-content/blob/main/Model%20Health%20Dashboard%20for%20ML%20Commons.png)


#### Are there breaking changes to the User Experience?

No

### What will it take to execute?
_Describe what it will take to build this feature. Are there any assumptions you may be making that could limit scope or add limitations? Are there performance, cost, or technical constraints that may impact the user experience? Does this feature depend on other feature work? What additional risks are there?_

Are there any assumptions you may be making that could limit scope or add limitations?

No

Are there performance, cost, or technical constraints that may impact the user experience?

No

Does this feature depend on other feature work? 

This feature is part of the ml-commons plug-in. You will need to install the plugin. You will also need to provision ML Nodes and deploy one or more models, or there will be nothing to display in the dashboard. Lastly, you will need permissions to run the underlying Profile API in order to see the dashboard.

What additional risks are there?

None


### Any remaining open questions?

We're looking foward to community feedback!

