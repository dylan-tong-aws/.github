---
name: 💭 Proposal
about: Suggest an idea for a specific feature you wish to propose to the community for comment
title: 'Machine Learning Model Access Controls'
labels: proposal
assignees: ''
---
## What/Why
### What are you proposing?

We are building model access controls for the ml-commons plugin, so that our users can govern who can perform actions on each ML model that is managed by our plugin. 

### What users have asked for this feature?

We’ve proactively decided to add this feature because we believe security is a job zero priority.

### What problems are you trying to solve?

Yes, the model access controls will be supported through the security plugin and use the same APIs used by other plugins to support resource level access controls. Here is the documentation for the anomaly detection plugin, which provides examples of how the security plugin APIs that can be used to configure backend roles for detectors. The ml-commons plugin will do the same for model groups which represent a collection of versions of the same model.

### What is the developer experience going to be?

The model access controls will be supported through the security plugin and use the same APIs used by other plugins to support resource level access controls. Here is the [documentation](https://opensearch.org/docs/latest/observing-your-data/ad/security/#advanced-limit-access-by-backend-role) for the anomaly detection plugin, which provides examples of how the security plugin APIs that can be used to configure backend roles for detectors. The ml-commons plugin will do the same for model groups which represent a collection of versions of the same model.

#### Are there any security considerations? 

This is a security enhancement.

#### Are there any breaking changes to the API

No

### What is the user experience going to be?

The user experience will be the same as what we provide in other plugins like anomaly detection and alerting. For example, the anomaly detection plugin’s admin process is described here.

The admin will associated backend roles to users and model groups. The users will gain the ability to perform the following actions on models that have at least one common backend role:


1. https://opensearch.org/docs/latest/ml-commons-plugin/api/#get-model-information
2. https://opensearch.org/docs/latest/ml-commons-plugin/api/#load-model
3. https://opensearch.org/docs/latest/ml-commons-plugin/api/#unload-a-model
4. https://opensearch.org/docs/latest/ml-commons-plugin/api/#search-model
5. https://opensearch.org/docs/latest/ml-commons-plugin/api/#delete-model
6. https://opensearch.org/docs/latest/ml-commons-plugin/api/#predict



#### Are there breaking changes to the User Experience?

No


### What will it take to execute?

Additional security features come at the cost. Additional access control checks will be required and the overhead can increase API execution time.


