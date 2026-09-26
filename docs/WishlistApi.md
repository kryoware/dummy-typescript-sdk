# WishlistApi

All URIs are relative to *http://petstore.swagger.io/v2*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createWishlistItem**](WishlistApi.md#createwishlistitem) | **POST** /wishlist | Save a pet |
| [**deleteWishlistItem**](WishlistApi.md#deletewishlistitem) | **DELETE** /wishlist/{id} | Remove a saved pet |
| [**getWishlistItem**](WishlistApi.md#getwishlistitem) | **GET** /wishlist/{id} | Get a saved pet |
| [**listWishlistItems**](WishlistApi.md#listwishlistitems) | **GET** /wishlist | List saved pets |
| [**updateWishlistItem**](WishlistApi.md#updatewishlistitem) | **PUT** /wishlist/{id} | Update a saved pet |



## createWishlistItem

> WishlistItem createWishlistItem(wishlistItem)

Save a pet

### Example

```ts
import {
  Configuration,
  WishlistApi,
} from '@iaybgu/petstore-sdk';
import type { CreateWishlistItemRequest } from '@iaybgu/petstore-sdk';

async function example() {
  console.log("🚀 Testing @iaybgu/petstore-sdk SDK...");
  const api = new WishlistApi();

  const body = {
    // WishlistItem
    wishlistItem: ...,
  } satisfies CreateWishlistItemRequest;

  try {
    const data = await api.createWishlistItem(body);
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
| **wishlistItem** | [WishlistItem](WishlistItem.md) |  | |

### Return type

[**WishlistItem**](WishlistItem.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Pet saved |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## deleteWishlistItem

> deleteWishlistItem(id)

Remove a saved pet

### Example

```ts
import {
  Configuration,
  WishlistApi,
} from '@iaybgu/petstore-sdk';
import type { DeleteWishlistItemRequest } from '@iaybgu/petstore-sdk';

async function example() {
  console.log("🚀 Testing @iaybgu/petstore-sdk SDK...");
  const api = new WishlistApi();

  const body = {
    // number
    id: 789,
  } satisfies DeleteWishlistItemRequest;

  try {
    const data = await api.deleteWishlistItem(body);
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
| **204** | Saved pet removed |  -  |
| **404** | Saved pet not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getWishlistItem

> WishlistItem getWishlistItem(id)

Get a saved pet

### Example

```ts
import {
  Configuration,
  WishlistApi,
} from '@iaybgu/petstore-sdk';
import type { GetWishlistItemRequest } from '@iaybgu/petstore-sdk';

async function example() {
  console.log("🚀 Testing @iaybgu/petstore-sdk SDK...");
  const api = new WishlistApi();

  const body = {
    // number
    id: 789,
  } satisfies GetWishlistItemRequest;

  try {
    const data = await api.getWishlistItem(body);
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

[**WishlistItem**](WishlistItem.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Saved pet |  -  |
| **404** | Saved pet not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listWishlistItems

> Array&lt;WishlistItem&gt; listWishlistItems()

List saved pets

### Example

```ts
import {
  Configuration,
  WishlistApi,
} from '@iaybgu/petstore-sdk';
import type { ListWishlistItemsRequest } from '@iaybgu/petstore-sdk';

async function example() {
  console.log("🚀 Testing @iaybgu/petstore-sdk SDK...");
  const api = new WishlistApi();

  try {
    const data = await api.listWishlistItems();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;WishlistItem&gt;**](WishlistItem.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Saved pets |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## updateWishlistItem

> WishlistItem updateWishlistItem(id, wishlistItem)

Update a saved pet

### Example

```ts
import {
  Configuration,
  WishlistApi,
} from '@iaybgu/petstore-sdk';
import type { UpdateWishlistItemRequest } from '@iaybgu/petstore-sdk';

async function example() {
  console.log("🚀 Testing @iaybgu/petstore-sdk SDK...");
  const api = new WishlistApi();

  const body = {
    // number
    id: 789,
    // WishlistItem
    wishlistItem: ...,
  } satisfies UpdateWishlistItemRequest;

  try {
    const data = await api.updateWishlistItem(body);
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
| **wishlistItem** | [WishlistItem](WishlistItem.md) |  | |

### Return type

[**WishlistItem**](WishlistItem.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Saved pet updated |  -  |
| **404** | Saved pet not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

