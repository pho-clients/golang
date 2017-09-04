# \DefaultApi

All URIs are relative to *https://virtserver.swaggerhub.com/phonetworks/server-rest/1.1.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddAttribute**](DefaultApi.md#AddAttribute) | **Post** /{uuid}/attribute/{key} | updates (or creates) an attribute
[**DelAttribute**](DefaultApi.md#DelAttribute) | **Delete** /{uuid}/attribute/{key} | deletes an attribute
[**DelEntity**](DefaultApi.md#DelEntity) | **Delete** /{uuid} | deletes an entity
[**GetAllEdges**](DefaultApi.md#GetAllEdges) | **Get** /{uuid}/edges/all | retrieves the edges of a node
[**GetAttribute**](DefaultApi.md#GetAttribute) | **Get** /{uuid}/attribute/{key} | retrieves the value of an entity attribute
[**GetAttributes**](DefaultApi.md#GetAttributes) | **Get** /{uuid}/attributes | retrieves the existing attribute keys of an entity (edge or node)
[**GetEdge**](DefaultApi.md#GetEdge) | **Get** /edge/{uuid} | retrieves an edge
[**GetEdgeGetters**](DefaultApi.md#GetEdgeGetters) | **Get** /{uuid}/edges/getters | retrieves the edge getter methods of a node
[**GetEdgeSetters**](DefaultApi.md#GetEdgeSetters) | **Get** /{uuid}/edges/setters | retrieves the edge setter methods of a node
[**GetFounder**](DefaultApi.md#GetFounder) | **Get** /founder | retrieves the Graph Founder
[**GetGraph**](DefaultApi.md#GetGraph) | **Get** /graph | retrieves the main Graph
[**GetIncomingEdges**](DefaultApi.md#GetIncomingEdges) | **Get** /{uuid}/edges/in | retrieves the incoming edges of a node
[**GetNode**](DefaultApi.md#GetNode) | **Get** /{uuid} | retrieves a node
[**GetNodeEdge**](DefaultApi.md#GetNodeEdge) | **Get** /{uuid}/{edge} | edge getter
[**GetOutgoingEdges**](DefaultApi.md#GetOutgoingEdges) | **Get** /{uuid}/edges/out | retrieves the outgoing edges of a node
[**GetSpace**](DefaultApi.md#GetSpace) | **Get** /space | retrieves the Space
[**GetType**](DefaultApi.md#GetType) | **Get** /{uuid}/type | fetches entity type
[**MakeActor**](DefaultApi.md#MakeActor) | **Post** /actor | creates an Actor object
[**MakeEdge**](DefaultApi.md#MakeEdge) | **Post** /{uuid}/{edge} | creates an edge
[**SetAttribute**](DefaultApi.md#SetAttribute) | **Put** /{uuid}/attribute/{key} | updates (or creates) an attribute


# **AddAttribute**
> InlineResponse2004 AddAttribute($value)

updates (or creates) an attribute

Works with all entities, including nodes and edges. Given its key, updates an  attribute value, or creates it, if it doesn't yet exist. 


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **value** | **string**| The value to update the key with. | [optional] 

### Return type

[**InlineResponse2004**](inline_response_200_4.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DelAttribute**
> InlineResponse2004 DelAttribute()

deletes an attribute

Works with all entities, including nodes and edges. Given its key, deletes an  attribute. 


### Parameters
This endpoint does not need any parameter.

### Return type

[**InlineResponse2004**](inline_response_200_4.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DelEntity**
> DelEntity()

deletes an entity

Works with all entities, including nodes and edges.  


### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetAllEdges**
> InlineResponse2003 GetAllEdges($uuid)

retrieves the edges of a node

By passing in a node ID, you can fetch all the edges of the node in question; including incoming and outgoing. 


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **string**| The node ID | 

### Return type

[**InlineResponse2003**](inline_response_200_3.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetAttribute**
> string GetAttribute($uuid, $key)

retrieves the value of an entity attribute

Attribute key must be case-sensitive. 


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **string**| The node ID | 
 **key** | **string**| The attribute key | 

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetAttributes**
> []string GetAttributes($uuid)

retrieves the existing attribute keys of an entity (edge or node)

Attribute keys are case-sensitive, and they will be listed in an array. 


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **string**| The node ID | 

### Return type

**[]string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetEdge**
> Edge GetEdge($uuid)

retrieves an edge

By passing in an ID, you can search for available edges in the system.  


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **string**| The edge ID | 

### Return type

[**Edge**](Edge.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetEdgeGetters**
> []string GetEdgeGetters($uuid)

retrieves the edge getter methods of a node

By passing in a node UUID that exists in the database, you can fetch  the edge getter methods of the node in question. 


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **string**| The node ID | 

### Return type

**[]string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetEdgeSetters**
> []string GetEdgeSetters($uuid)

retrieves the edge setter methods of a node

By passing in a node UUID that exists in the database, you can fetch  the edge setter methods of the node in question. These setters may or  may not be formative. If they are formative, a new node is created in result. 


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **string**| The node ID | 

### Return type

**[]string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetFounder**
> InlineResponse200 GetFounder()

retrieves the Graph Founder

The Founder must be a \\Pho\\Framework\\Actor object.  This method returns the object type as well as object ID. 


### Parameters
This endpoint does not need any parameter.

### Return type

[**InlineResponse200**](inline_response_200.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetGraph**
> InlineResponse2001 GetGraph()

retrieves the main Graph

The Graph must be a \\Pho\\Lib\\Graph\\SubGraph and \\Pho\\Framework\\Graph object.  This method returns the object type as well as object ID. The Graph contains all nodes and edges in the system.  Though it is contained by Space, its one and only container. 


### Parameters
This endpoint does not need any parameter.

### Return type

[**InlineResponse2001**](inline_response_200_1.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetIncomingEdges**
> []NodeEdge GetIncomingEdges($uuid)

retrieves the incoming edges of a node

By passing in a node ID, you can fetch  the incoming edges of the node in question. 


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **string**| the node ID | 

### Return type

[**[]NodeEdge**](NodeEdge.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetNode**
> Node GetNode($uuid)

retrieves a node

By passing in an ID, you can search for available nodes in the system. Please note, this function will not return edges. This method  is  reserved for nodes only.  


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **string**| The node ID | 

### Return type

[**Node**](Node.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetNodeEdge**
> []string GetNodeEdge($uuid, $edge)

edge getter

Fetches edge results, whether as edge IDs or node IDs, depending on edge's characteristics.  


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **string**| The node ID | 
 **edge** | **string**| The edge getter label | 

### Return type

**[]string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetOutgoingEdges**
> []NodeEdge GetOutgoingEdges($uuid)

retrieves the outgoing edges of a node

By passing in a node ID, you can fetch  the outgoing edges of the node in question. 


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **string**| the node ID | 

### Return type

[**[]NodeEdge**](NodeEdge.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetSpace**
> InlineResponse2002 GetSpace()

retrieves the Space

The Space must be a \\Pho\\Lib\\Graph\\Graph object.  This method returns the object type as well as object uuid. Space always comes with the nil ID;  00000000000000000000000000000000, and under normal circumstances its class is always Pho\\Kernel\\Standards\\Space 


### Parameters
This endpoint does not need any parameter.

### Return type

[**InlineResponse2002**](inline_response_200_2.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetType**
> string GetType($uuid)

fetches entity type

Possible values are; \"Space\", \"Node\", \"Graph Node\", \"Graph\", \"Actor Node\" \"Object Node\", \"Edge\", \"Read Edge\", \"Write Edge\", \"Subscribe Edge\", \"Mention Edge\", \"Unidentified\". 


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | **string**| the node | 

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MakeActor**
> string MakeActor($param1)

creates an Actor object

Fetches whatever set as \"default_object\"=>\"actor\" while determining what Actor object to construct. If it doesn't exist, uses \"default_object\"=>\"founder\" class. Otherwise fails. 


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **param1** | **string**| Actor constructor argument. More parameters may be passed via param2, param3 ... param50.  | [optional] 

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **MakeEdge**
> string MakeEdge($param1)

creates an edge

Used to set new edges. If the edge is formative, then a node is also formed. 


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **param1** | **string**| The value to update the key with. There can be 50 of those. For example;  param1&#x3D;\&quot;value1\&quot;, param2 &#x3D;\&quot;another value\&quot; depending on the edge&#39;s default constructor variable count.  | [optional] 

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **SetAttribute**
> InlineResponse2004 SetAttribute($value)

updates (or creates) an attribute

Works with all entities, including nodes and edges. Given its key, updates an  attribute value, or creates it, if it doesn't yet exist. 


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **value** | **string**| The value to update the key with. | [optional] 

### Return type

[**InlineResponse2004**](inline_response_200_4.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

