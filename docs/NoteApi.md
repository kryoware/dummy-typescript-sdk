# NoteApi

All URIs are relative to *http://petstore.swagger.io/v2*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createNote**](NoteApi.md#createnote) | **POST** /notes | Create a pet note |
| [**deleteNote**](NoteApi.md#deletenote) | **DELETE** /notes/{id} | Delete a pet note |
| [**getNote**](NoteApi.md#getnote) | **GET** /notes/{id} | Get a pet note |
| [**updateNote**](NoteApi.md#updatenote) | **PUT** /notes/{id} | Update a pet note |



## createNote

> PetNote createNote(petNote)

Create a pet note

### Example

```ts
import {
  Configuration,
  NoteApi,
} from '@iaybgu/petstore-sdk';
import type { CreateNoteRequest } from '@iaybgu/petstore-sdk';

async function example() {
  console.log("🚀 Testing @iaybgu/petstore-sdk SDK...");
  const api = new NoteApi();

  const body = {
    // PetNote
    petNote: ...,
  } satisfies CreateNoteRequest;

  try {
    const data = await api.createNote(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **petNote** | [PetNote](PetNote.md) |  | |

### Return type

[**PetNote**](PetNote.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Note created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## deleteNote

> deleteNote(id)

Delete a pet note

### Example

```ts
import {
  Configuration,
  NoteApi,
} from '@iaybgu/petstore-sdk';
import type { DeleteNoteRequest } from '@iaybgu/petstore-sdk';

async function example() {
  console.log("🚀 Testing @iaybgu/petstore-sdk SDK...");
  const api = new NoteApi();

  const body = {
    // number
    id: 789,
  } satisfies DeleteNoteRequest;

  try {
    const data = await api.deleteNote(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | `number` |  | [Defaults to `undefined`] |

### Return type

`void` (Empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Note deleted |  -  |
| **404** | Note not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getNote

> PetNote getNote(id)

Get a pet note

### Example

```ts
import {
  Configuration,
  NoteApi,
} from '@iaybgu/petstore-sdk';
import type { GetNoteRequest } from '@iaybgu/petstore-sdk';

async function example() {
  console.log("🚀 Testing @iaybgu/petstore-sdk SDK...");
  const api = new NoteApi();

  const body = {
    // number
    id: 789,
  } satisfies GetNoteRequest;

  try {
    const data = await api.getNote(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | `number` |  | [Defaults to `undefined`] |

### Return type

[**PetNote**](PetNote.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Pet note |  -  |
| **404** | Note not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## updateNote

> PetNote updateNote(id, petNote)

Update a pet note

### Example

```ts
import {
  Configuration,
  NoteApi,
} from '@iaybgu/petstore-sdk';
import type { UpdateNoteRequest } from '@iaybgu/petstore-sdk';

async function example() {
  console.log("🚀 Testing @iaybgu/petstore-sdk SDK...");
  const api = new NoteApi();

  const body = {
    // number
    id: 789,
    // PetNote
    petNote: ...,
  } satisfies UpdateNoteRequest;

  try {
    const data = await api.updateNote(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | `number` |  | [Defaults to `undefined`] |
| **petNote** | [PetNote](PetNote.md) |  | |

### Return type

[**PetNote**](PetNote.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Note updated |  -  |
| **404** | Note not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

