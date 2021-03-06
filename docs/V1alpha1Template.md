# V1alpha1Template

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**active_deadline_seconds** | **int** | Optional duration in seconds relative to the StartTime that the pod may be active on a node before the system actively tries to terminate the pod; value must be positive integer This field is only applicable to container and script templates. | [optional] 
**affinity** | [**IoK8sApiCoreV1Affinity**](IoK8sApiCoreV1Affinity.md) | Affinity sets the pod&#39;s scheduling constraints Overrides the affinity set at the workflow level (if any) | [optional] 
**archive_location** | [**V1alpha1ArtifactLocation**](V1alpha1ArtifactLocation.md) | Location in which all files related to the step will be stored (logs, artifacts, etc...). Can be overridden by individual items in Outputs. If omitted, will use the default artifact repository location configured in the controller, appended with the &lt;workflowname&gt;/&lt;nodename&gt; in the key. | [optional] 
**arguments** | [**V1alpha1Arguments**](V1alpha1Arguments.md) | Arguments hold arguments to the template. | [optional] 
**automount_service_account_token** | **bool** | AutomountServiceAccountToken indicates whether a service account token should be automatically mounted in pods. ServiceAccountName of ExecutorConfig must be specified if this value is false. | [optional] 
**container** | [**IoK8sApiCoreV1Container**](IoK8sApiCoreV1Container.md) | Container is the main container image to run in the pod | [optional] 
**daemon** | **bool** | Deamon will allow a workflow to proceed to the next step so long as the container reaches readiness | [optional] 
**dag** | [**V1alpha1DAGTemplate**](V1alpha1DAGTemplate.md) | DAG template subtype which runs a DAG | [optional] 
**executor** | [**V1alpha1ExecutorConfig**](V1alpha1ExecutorConfig.md) | Executor holds configurations of the executor container. | [optional] 
**host_aliases** | [**list[IoK8sApiCoreV1HostAlias]**](IoK8sApiCoreV1HostAlias.md) | HostAliases is an optional list of hosts and IPs that will be injected into the pod spec | [optional] 
**init_containers** | [**list[V1alpha1UserContainer]**](V1alpha1UserContainer.md) | InitContainers is a list of containers which run before the main container. | [optional] 
**inputs** | [**V1alpha1Inputs**](V1alpha1Inputs.md) | Inputs describe what inputs parameters and artifacts are supplied to this template | [optional] 
**metadata** | [**V1alpha1Metadata**](V1alpha1Metadata.md) | Metdata sets the pods&#39;s metadata, i.e. annotations and labels | [optional] 
**name** | **str** | Name is the name of the template | 
**node_selector** | **dict(str, str)** | NodeSelector is a selector to schedule this step of the workflow to be run on the selected node(s). Overrides the selector set at the workflow level. | [optional] 
**outputs** | [**V1alpha1Outputs**](V1alpha1Outputs.md) | Outputs describe the parameters and artifacts that this template produces | [optional] 
**parallelism** | **int** | Parallelism limits the max total parallel pods that can execute at the same time within the boundaries of this template invocation. If additional steps/dag templates are invoked, the pods created by those templates will not be counted towards this total. | [optional] 
**pod_spec_patch** | **str** | PodSpecPatch holds strategic merge patch to apply against the pod spec. Allows parameterization of container fields which are not strings (e.g. resource limits). | [optional] 
**priority** | **int** | Priority to apply to workflow pods. | [optional] 
**priority_class_name** | **str** | PriorityClassName to apply to workflow pods. | [optional] 
**resource** | [**V1alpha1ResourceTemplate**](V1alpha1ResourceTemplate.md) | Resource template subtype which can run k8s resources | [optional] 
**retry_strategy** | [**V1alpha1RetryStrategy**](V1alpha1RetryStrategy.md) | RetryStrategy describes how to retry a template when it fails | [optional] 
**scheduler_name** | **str** | If specified, the pod will be dispatched by specified scheduler. Or it will be dispatched by workflow scope scheduler if specified. If neither specified, the pod will be dispatched by default scheduler. | [optional] 
**script** | [**V1alpha1ScriptTemplate**](V1alpha1ScriptTemplate.md) | Script runs a portion of code against an interpreter | [optional] 
**security_context** | [**IoK8sApiCoreV1PodSecurityContext**](IoK8sApiCoreV1PodSecurityContext.md) | SecurityContext holds pod-level security attributes and common container settings. Optional: Defaults to empty.  See type description for default values of each field. | [optional] 
**service_account_name** | **str** | ServiceAccountName to apply to workflow pods | [optional] 
**sidecars** | [**list[V1alpha1UserContainer]**](V1alpha1UserContainer.md) | Sidecars is a list of containers which run alongside the main container Sidecars are automatically killed when the main container completes | [optional] 
**steps** | [**list[V1alpha1ParallelSteps]**](V1alpha1ParallelSteps.md) | Steps define a series of sequential/parallel workflow steps | [optional] 
**suspend** | [**V1alpha1SuspendTemplate**](V1alpha1SuspendTemplate.md) | Suspend template subtype which can suspend a workflow when reaching the step | [optional] 
**template** | **str** | Template is the name of the template which is used as the base of this template. | [optional] 
**template_ref** | [**V1alpha1TemplateRef**](V1alpha1TemplateRef.md) | TemplateRef is the reference to the template resource which is used as the base of this template. | [optional] 
**tolerations** | [**list[IoK8sApiCoreV1Toleration]**](IoK8sApiCoreV1Toleration.md) | Tolerations to apply to workflow pods. | [optional] 
**volumes** | [**list[IoK8sApiCoreV1Volume]**](IoK8sApiCoreV1Volume.md) | Volumes is a list of volumes that can be mounted by containers in a template. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


