# postboost.AgentsApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**approve_agent_proposal**](AgentsApi.md#approve_agent_proposal) | **POST** /{workspaceUuid}/agent-proposals/{proposalUuid}/approve | Approve and apply an agent proposal
[**create_agent**](AgentsApi.md#create_agent) | **POST** /{workspaceUuid}/agents | Switch on a background agent
[**delete_agent**](AgentsApi.md#delete_agent) | **DELETE** /{workspaceUuid}/agents/{agentUuid} | Delete a background agent
[**get_agent_run**](AgentsApi.md#get_agent_run) | **GET** /{workspaceUuid}/agent-runs/{runUuid} | Get an agent run with its proposals
[**list_agent_proposals**](AgentsApi.md#list_agent_proposals) | **GET** /{workspaceUuid}/agent-proposals | List agent proposals (approval queue)
[**list_agent_runs**](AgentsApi.md#list_agent_runs) | **GET** /{workspaceUuid}/agents/{agentUuid}/runs | Run history of an agent
[**list_agents**](AgentsApi.md#list_agents) | **GET** /{workspaceUuid}/agents | List background agents
[**reject_agent_proposal**](AgentsApi.md#reject_agent_proposal) | **POST** /{workspaceUuid}/agent-proposals/{proposalUuid}/reject | Reject an agent proposal
[**run_agent**](AgentsApi.md#run_agent) | **POST** /{workspaceUuid}/agents/{agentUuid}/run | Run a background agent now
[**update_agent**](AgentsApi.md#update_agent) | **PUT** /{workspaceUuid}/agents/{agentUuid} | Update a background agent


# **approve_agent_proposal**
> ApproveAgentProposal200Response approve_agent_proposal(workspace_uuid, proposal_uuid, agent_proposal_decision=agent_proposal_decision)

Approve and apply an agent proposal

Applies the proposal at once: `hold_post` moves the post back to draft, `edit_caption` replaces the caption, `retry_account` saves the shortened caption (if any) on that account's version and publishes that account again, `reconnect_account` only records the decision. When the post was edited, deleted or left the schedule since the proposal was made (for `retry_account`: the account is no longer failed, the post is publishing, or the plan does not allow scheduling), nothing changes and the proposal becomes `stale`. Admins and members only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.agent_proposal_decision import AgentProposalDecision
from postboost.models.approve_agent_proposal200_response import ApproveAgentProposal200Response
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.AgentsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    proposal_uuid = 'proposal_uuid_example' # str | 
    agent_proposal_decision = postboost.AgentProposalDecision() # AgentProposalDecision |  (optional)

    try:
        # Approve and apply an agent proposal
        api_response = api_instance.approve_agent_proposal(workspace_uuid, proposal_uuid, agent_proposal_decision=agent_proposal_decision)
        print("The response of AgentsApi->approve_agent_proposal:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->approve_agent_proposal: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **proposal_uuid** | **str**|  | 
 **agent_proposal_decision** | [**AgentProposalDecision**](AgentProposalDecision.md)|  | [optional] 

### Return type

[**ApproveAgentProposal200Response**](ApproveAgentProposal200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Decision recorded; read &#x60;data.status&#x60; (&#x60;applied&#x60;, &#x60;stale&#x60; or &#x60;failed&#x60;) |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**409** | The proposal was already decided, expired or went stale; &#x60;data&#x60; is its current state. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_agent**
> CreateAgent201Response create_agent(workspace_uuid, workspace_agent_input)

Switch on a background agent

Creates an agent (one per type per workspace). It first runs within five minutes, then on its `schedule`. **Pre-publish checker** looks at posts scheduled in the next `horizon_hours` and proposes holding (back to draft) posts that would fail: disconnected accounts, network requirements, daily caps, the X allowance and links that answer an error. It proposes caption edits that drop `banned_phrases`. With `ai_review: true` it also asks AI to review up to `max_ai_reviews_per_run` posts per run (one AI credit each). **Failed-post fixer** looks at posts that failed on an account in the last `lookback_hours` and proposes, per post and account, `reconnect_account` (the account's token expired), or `retry_account`, with a caption trimmed to the network limit when the text is over it. One open proposal per post and account. It uses no AI. Admins and members only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_agent201_response import CreateAgent201Response
from postboost.models.workspace_agent_input import WorkspaceAgentInput
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.AgentsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    workspace_agent_input = {"type":"pre_publish_checker","schedule":"hourly","settings":{"horizon_hours":24,"banned_phrases":["guaranteed"]}} # WorkspaceAgentInput | 

    try:
        # Switch on a background agent
        api_response = api_instance.create_agent(workspace_uuid, workspace_agent_input)
        print("The response of AgentsApi->create_agent:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->create_agent: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **workspace_agent_input** | [**WorkspaceAgentInput**](WorkspaceAgentInput.md)|  | 

### Return type

[**CreateAgent201Response**](CreateAgent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Agent created |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_agent**
> DeleteAgent200Response delete_agent(workspace_uuid, agent_uuid)

Delete a background agent

Removes the agent. Its run history and proposals stay. Admins and members only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.delete_agent200_response import DeleteAgent200Response
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.AgentsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    agent_uuid = 'agent_uuid_example' # str | 

    try:
        # Delete a background agent
        api_response = api_instance.delete_agent(workspace_uuid, agent_uuid)
        print("The response of AgentsApi->delete_agent:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->delete_agent: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **agent_uuid** | **str**|  | 

### Return type

[**DeleteAgent200Response**](DeleteAgent200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Agent deleted |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_agent_run**
> RunAgent202Response get_agent_run(workspace_uuid, run_uuid)

Get an agent run with its proposals

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.run_agent202_response import RunAgent202Response
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.AgentsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    run_uuid = 'run_uuid_example' # str | 

    try:
        # Get an agent run with its proposals
        api_response = api_instance.get_agent_run(workspace_uuid, run_uuid)
        print("The response of AgentsApi->get_agent_run:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->get_agent_run: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **run_uuid** | **str**|  | 

### Return type

[**RunAgent202Response**](RunAgent202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Run |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_agent_proposals**
> ListAgentProposals200Response list_agent_proposals(workspace_uuid, status=status, per_page=per_page, page=page)

List agent proposals (approval queue)

Proposals of all agents in the workspace, newest first. Defaults to `pending`.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_agent_proposals200_response import ListAgentProposals200Response
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.AgentsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    status = pending # str |  (optional) (default to pending)
    per_page = 20 # int |  (optional) (default to 20)
    page = 56 # int |  (optional)

    try:
        # List agent proposals (approval queue)
        api_response = api_instance.list_agent_proposals(workspace_uuid, status=status, per_page=per_page, page=page)
        print("The response of AgentsApi->list_agent_proposals:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->list_agent_proposals: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **status** | **str**|  | [optional] [default to pending]
 **per_page** | **int**|  | [optional] [default to 20]
 **page** | **int**|  | [optional] 

### Return type

[**ListAgentProposals200Response**](ListAgentProposals200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Proposals |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_agent_runs**
> ListAgentRuns200Response list_agent_runs(workspace_uuid, agent_uuid, per_page=per_page, page=page)

Run history of an agent

Runs of the agent, newest first, with what each checked and proposed and the AI credits it used.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_agent_runs200_response import ListAgentRuns200Response
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.AgentsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    agent_uuid = 'agent_uuid_example' # str | 
    per_page = 20 # int |  (optional) (default to 20)
    page = 56 # int |  (optional)

    try:
        # Run history of an agent
        api_response = api_instance.list_agent_runs(workspace_uuid, agent_uuid, per_page=per_page, page=page)
        print("The response of AgentsApi->list_agent_runs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->list_agent_runs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **agent_uuid** | **str**|  | 
 **per_page** | **int**|  | [optional] [default to 20]
 **page** | **int**|  | [optional] 

### Return type

[**ListAgentRuns200Response**](ListAgentRuns200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Runs |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_agents**
> ListAgents200Response list_agents(workspace_uuid)

List background agents

Background agents switched on for the workspace. Agents run on a schedule, record every run and never change a post themselves: each change is a proposal that a workspace admin or member approves. Available types: `pre_publish_checker`, `failed_post_fixer`. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_agents200_response import ListAgents200Response
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.AgentsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # List background agents
        api_response = api_instance.list_agents(workspace_uuid)
        print("The response of AgentsApi->list_agents:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->list_agents: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

### Return type

[**ListAgents200Response**](ListAgents200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Agents |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reject_agent_proposal**
> ApproveAgentProposal200Response reject_agent_proposal(workspace_uuid, proposal_uuid, agent_proposal_decision=agent_proposal_decision)

Reject an agent proposal

Records the rejection (and optional note); nothing changes on the post. Admins and members only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.agent_proposal_decision import AgentProposalDecision
from postboost.models.approve_agent_proposal200_response import ApproveAgentProposal200Response
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.AgentsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    proposal_uuid = 'proposal_uuid_example' # str | 
    agent_proposal_decision = postboost.AgentProposalDecision() # AgentProposalDecision |  (optional)

    try:
        # Reject an agent proposal
        api_response = api_instance.reject_agent_proposal(workspace_uuid, proposal_uuid, agent_proposal_decision=agent_proposal_decision)
        print("The response of AgentsApi->reject_agent_proposal:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->reject_agent_proposal: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **proposal_uuid** | **str**|  | 
 **agent_proposal_decision** | [**AgentProposalDecision**](AgentProposalDecision.md)|  | [optional] 

### Return type

[**ApproveAgentProposal200Response**](ApproveAgentProposal200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Proposal rejected |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**409** | The proposal was already decided, expired or went stale; &#x60;data&#x60; is its current state. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **run_agent**
> RunAgent202Response run_agent(workspace_uuid, agent_uuid)

Run a background agent now

Queues a run outside the schedule (`trigger: manual`). Six per hour. Admins and members only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.run_agent202_response import RunAgent202Response
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.AgentsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    agent_uuid = 'agent_uuid_example' # str | 

    try:
        # Run a background agent now
        api_response = api_instance.run_agent(workspace_uuid, agent_uuid)
        print("The response of AgentsApi->run_agent:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->run_agent: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **agent_uuid** | **str**|  | 

### Return type

[**RunAgent202Response**](RunAgent202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Run queued |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**409** | The agent already has a queued or running run. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_agent**
> CreateAgent201Response update_agent(workspace_uuid, agent_uuid, workspace_agent_update)

Update a background agent

Changes the name, schedule, settings or `enabled`. Settings you leave out keep their value. Admins and members only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_agent201_response import CreateAgent201Response
from postboost.models.workspace_agent_update import WorkspaceAgentUpdate
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.AgentsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    agent_uuid = 'agent_uuid_example' # str | 
    workspace_agent_update = postboost.WorkspaceAgentUpdate() # WorkspaceAgentUpdate | 

    try:
        # Update a background agent
        api_response = api_instance.update_agent(workspace_uuid, agent_uuid, workspace_agent_update)
        print("The response of AgentsApi->update_agent:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->update_agent: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **agent_uuid** | **str**|  | 
 **workspace_agent_update** | [**WorkspaceAgentUpdate**](WorkspaceAgentUpdate.md)|  | 

### Return type

[**CreateAgent201Response**](CreateAgent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Agent updated |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

