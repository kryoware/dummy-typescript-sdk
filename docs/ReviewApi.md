# ReviewApi

All URIs are relative to *http://petstore.swagger.io/v2*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createReview**](ReviewApi.md#createreview) | **POST** /reviews | Create a pet review |
| [**deleteReview**](ReviewApi.md#deletereview) | **DELETE** /reviews/{id} | Delete a pet review |
| [**getReview**](ReviewApi.md#getreview) | **GET** /reviews/{id} | Get a pet review |
| [**updateReview**](ReviewApi.md#updatereview) | **PUT** /reviews/{id} | Update a pet review |



## createReview

> Review createReview(review)

Create a pet review

### Example

```ts
import {
  Configuration,
  ReviewApi,
} from '@iaybgu/petstore-sdk';
import type { CreateReviewRequest } from '@iaybgu/petstore-sdk';

async function example() {
  console.log("🚀 Testing @iaybgu/petstore-sdk SDK...");
  const api = new ReviewApi();

  const body = {
    // Review
    review: ...,
  } satisfies CreateReviewRequest;

  try {
    const data = await api.createReview(body);
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
| **review** | [Review](Review.md) |  | |

### Return type

[**Review**](Review.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Review created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## deleteReview

> deleteReview(id)

Delete a pet review

### Example

```ts
import {
  Configuration,
  ReviewApi,
} from '@iaybgu/petstore-sdk';
import type { DeleteReviewRequest } from '@iaybgu/petstore-sdk';

async function example() {
  console.log("🚀 Testing @iaybgu/petstore-sdk SDK...");
  const api = new ReviewApi();

  const body = {
    // number
    id: 789,
  } satisfies DeleteReviewRequest;

  try {
    const data = await api.deleteReview(body);
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
| **204** | Review deleted |  -  |
| **404** | Review not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getReview

> Review getReview(id)

Get a pet review

### Example

```ts
import {
  Configuration,
  ReviewApi,
} from '@iaybgu/petstore-sdk';
import type { GetReviewRequest } from '@iaybgu/petstore-sdk';

async function example() {
  console.log("🚀 Testing @iaybgu/petstore-sdk SDK...");
  const api = new ReviewApi();

  const body = {
    // number
    id: 789,
  } satisfies GetReviewRequest;

  try {
    const data = await api.getReview(body);
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

[**Review**](Review.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Pet review |  -  |
| **404** | Review not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## updateReview

> Review updateReview(id, review)

Update a pet review

### Example

```ts
import {
  Configuration,
  ReviewApi,
} from '@iaybgu/petstore-sdk';
import type { UpdateReviewRequest } from '@iaybgu/petstore-sdk';

async function example() {
  console.log("🚀 Testing @iaybgu/petstore-sdk SDK...");
  const api = new ReviewApi();

  const body = {
    // number
    id: 789,
    // Review
    review: ...,
  } satisfies UpdateReviewRequest;

  try {
    const data = await api.updateReview(body);
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
| **review** | [Review](Review.md) |  | |

### Return type

[**Review**](Review.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Review updated |  -  |
| **404** | Review not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

