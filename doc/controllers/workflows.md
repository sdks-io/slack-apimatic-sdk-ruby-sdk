# Workflows

```ruby
workflows_api = client.workflows
```

## Class Name

`WorkflowsApi`

## Methods

* [Workflows Step Completed](../../doc/controllers/workflows.md#workflows-step-completed)
* [Workflows Step Failed](../../doc/controllers/workflows.md#workflows-step-failed)
* [Workflows Update Step](../../doc/controllers/workflows.md#workflows-update-step)


# Workflows Step Completed

Indicate that an app's step in a workflow completed execution.

API method documentation: [https://api.slack.com/methods/workflows.stepCompleted](https://api.slack.com/methods/workflows.stepCompleted)

```ruby
def workflows_step_completed(token,
                             workflow_step_execute_id,
                             outputs: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `workflow.steps:execute` |
| `workflow_step_execute_id` | `String` | Query, Required | Context identifier that maps to the correct workflow step execution. |
| `outputs` | `String` | Query, Optional | Key-value object of outputs from your step. Keys of this object reflect the configured `key` properties of your [`outputs`](/reference/workflows/workflow_step#output) array from your `workflow_step` object. |

## Requires scope

### slackAuth

`workflow.steps:execute`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

workflow_step_execute_id = 'workflow_step_execute_id2'

result = workflows_api.workflows_step_completed(
  token,
  workflow_step_execute_id
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`DefaultErrorTemplateException`](../../doc/models/default-error-template-exception.md) |


# Workflows Step Failed

Indicate that an app's step in a workflow failed to execute.

API method documentation: [https://api.slack.com/methods/workflows.stepFailed](https://api.slack.com/methods/workflows.stepFailed)

```ruby
def workflows_step_failed(token,
                          workflow_step_execute_id,
                          error)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `workflow.steps:execute` |
| `workflow_step_execute_id` | `String` | Query, Required | Context identifier that maps to the correct workflow step execution. |
| `error` | `String` | Query, Required | A JSON-based object with a `message` property that should contain a human readable error message. |

## Requires scope

### slackAuth

`workflow.steps:execute`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

workflow_step_execute_id = 'workflow_step_execute_id2'

error = 'error4'

result = workflows_api.workflows_step_failed(
  token,
  workflow_step_execute_id,
  error
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`DefaultErrorTemplateException`](../../doc/models/default-error-template-exception.md) |


# Workflows Update Step

Update the configuration for a workflow extension step.

API method documentation: [https://api.slack.com/methods/workflows.updateStep](https://api.slack.com/methods/workflows.updateStep)

```ruby
def workflows_update_step(token,
                          workflow_step_edit_id,
                          inputs: nil,
                          outputs: nil,
                          step_name: nil,
                          step_image_url: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `workflow.steps:execute` |
| `workflow_step_edit_id` | `String` | Query, Required | A context identifier provided with `view_submission` payloads used to call back to `workflows.updateStep`. |
| `inputs` | `String` | Query, Optional | A JSON key-value map of inputs required from a user during configuration. This is the data your app expects to receive when the workflow step starts. **Please note**: the embedded variable format is set and replaced by the workflow system. You cannot create custom variables that will be replaced at runtime. [Read more about variables in workflow steps here](/workflows/steps#variables). |
| `outputs` | `String` | Query, Optional | An JSON array of output objects used during step execution. This is the data your app agrees to provide when your workflow step was executed. |
| `step_name` | `String` | Query, Optional | An optional field that can be used to override the step name that is shown in the Workflow Builder. |
| `step_image_url` | `String` | Query, Optional | An optional field that can be used to override app image that is shown in the Workflow Builder. |

## Requires scope

### slackAuth

`workflow.steps:execute`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

workflow_step_edit_id = 'workflow_step_edit_id0'

result = workflows_api.workflows_update_step(
  token,
  workflow_step_edit_id
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`DefaultErrorTemplateException`](../../doc/models/default-error-template-exception.md) |

