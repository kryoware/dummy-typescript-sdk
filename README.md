# @iaybgu/petstore-sdk@0.1.2

A TypeScript SDK client for the petstore.swagger.io API.

## Usage

First, install the SDK from npm.

```bash
npm install @iaybgu/petstore-sdk --save
```

Next, try it out.


```ts
import {
  Configuration,
  PetApi,
} from '@iaybgu/petstore-sdk';
import type { AddPetRequest } from '@iaybgu/petstore-sdk';

async function example() {
  console.log("🚀 Testing @iaybgu/petstore-sdk SDK...");
  const config = new Configuration({ 
    // To configure OAuth2 access token for authorization: petstore_auth implicit
    accessToken: "YOUR ACCESS TOKEN",
  });
  const api = new PetApi(config);

  const body = {
    // Pet | Pet object that needs to be added to the store
    pet: ...,
  } satisfies AddPetRequest;

  try {
    const data = await api.addPet(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```


## Documentation

### API Endpoints

All URIs are relative to *http://petstore.swagger.io/v2*

| Class | Method | HTTP request | Description
| ----- | ------ | ------------ | -------------
*PetApi* | [**addPet**](docs/PetApi.md#addpet) | **POST** /pet | Add a new pet to the store
*PetApi* | [**deletePet**](docs/PetApi.md#deletepet) | **DELETE** /pet/{petId} | Deletes a pet
*PetApi* | [**findPetsByStatus**](docs/PetApi.md#findpetsbystatus) | **GET** /pet/findByStatus | Finds Pets by status
*PetApi* | [**findPetsByTags**](docs/PetApi.md#findpetsbytags) | **GET** /pet/findByTags | Finds Pets by tags
*PetApi* | [**getPetById**](docs/PetApi.md#getpetbyid) | **GET** /pet/{petId} | Find pet by ID
*PetApi* | [**updatePet**](docs/PetApi.md#updatepet) | **PUT** /pet | Update an existing pet
*PetApi* | [**updatePetWithForm**](docs/PetApi.md#updatepetwithform) | **POST** /pet/{petId} | Updates a pet in the store with form data
*PetApi* | [**uploadFile**](docs/PetApi.md#uploadfile) | **POST** /pet/{petId}/uploadImage | uploads an image
*ReviewApi* | [**createReview**](docs/ReviewApi.md#createreview) | **POST** /reviews | Create a pet review
*ReviewApi* | [**deleteReview**](docs/ReviewApi.md#deletereview) | **DELETE** /reviews/{id} | Delete a pet review
*ReviewApi* | [**getReview**](docs/ReviewApi.md#getreview) | **GET** /reviews/{id} | Get a pet review
*ReviewApi* | [**updateReview**](docs/ReviewApi.md#updatereview) | **PUT** /reviews/{id} | Update a pet review
*StoreApi* | [**deleteOrder**](docs/StoreApi.md#deleteorder) | **DELETE** /store/order/{orderId} | Delete purchase order by ID
*StoreApi* | [**getInventory**](docs/StoreApi.md#getinventory) | **GET** /store/inventory | Returns pet inventories by status
*StoreApi* | [**getOrderById**](docs/StoreApi.md#getorderbyid) | **GET** /store/order/{orderId} | Find purchase order by ID
*StoreApi* | [**placeOrder**](docs/StoreApi.md#placeorder) | **POST** /store/order | Place an order for a pet
*UserApi* | [**createUser**](docs/UserApi.md#createuser) | **POST** /user | Create user
*UserApi* | [**createUsersWithArrayInput**](docs/UserApi.md#createuserswitharrayinput) | **POST** /user/createWithArray | Creates list of users with given input array
*UserApi* | [**createUsersWithListInput**](docs/UserApi.md#createuserswithlistinput) | **POST** /user/createWithList | Creates list of users with given input array
*UserApi* | [**deleteUser**](docs/UserApi.md#deleteuser) | **DELETE** /user/{username} | Delete user
*UserApi* | [**getUserByName**](docs/UserApi.md#getuserbyname) | **GET** /user/{username} | Get user by user name
*UserApi* | [**loginUser**](docs/UserApi.md#loginuser) | **GET** /user/login | Logs user into the system
*UserApi* | [**logoutUser**](docs/UserApi.md#logoutuser) | **GET** /user/logout | Logs out current logged in user session
*UserApi* | [**updateUser**](docs/UserApi.md#updateuser) | **PUT** /user/{username} | Updated user
*WishlistApi* | [**createWishlistItem**](docs/WishlistApi.md#createwishlistitem) | **POST** /wishlist | Save a pet
*WishlistApi* | [**deleteWishlistItem**](docs/WishlistApi.md#deletewishlistitem) | **DELETE** /wishlist/{id} | Remove a saved pet
*WishlistApi* | [**getWishlistItem**](docs/WishlistApi.md#getwishlistitem) | **GET** /wishlist/{id} | Get a saved pet
*WishlistApi* | [**listWishlistItems**](docs/WishlistApi.md#listwishlistitems) | **GET** /wishlist | List saved pets
*WishlistApi* | [**updateWishlistItem**](docs/WishlistApi.md#updatewishlistitem) | **PUT** /wishlist/{id} | Update a saved pet


### Models

- [Category](docs/Category.md)
- [ModelApiResponse](docs/ModelApiResponse.md)
- [Order](docs/Order.md)
- [Pet](docs/Pet.md)
- [Review](docs/Review.md)
- [Tag](docs/Tag.md)
- [User](docs/User.md)
- [WishlistItem](docs/WishlistItem.md)

### Authorization


Authentication schemes defined for the API:
<a id="petstore_auth-implicit"></a>
#### petstore_auth implicit


- **Type**: OAuth
- **Flow**: implicit
- **Authorization URL**: http://petstore.swagger.io/api/oauth/dialog
- **Scopes**: 
  - `write:pets`: modify pets in your account
  - `read:pets`: read your pets
<a id="api_key"></a>
#### api_key


- **Type**: API key
- **API key parameter name**: `api_key`
- **Location**: HTTP header

## About

This TypeScript SDK client supports the [Fetch API](https://fetch.spec.whatwg.org/)
and is automatically generated by the
[OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.0.0`
- Package version: `0.1.2`
- Generator version: `7.25.0`
- Build package: `org.openapitools.codegen.languages.TypeScriptFetchClientCodegen`

The generated npm module supports the following:

- Environments
  * Node.js
  * Webpack
  * Browserify
- Language levels
  * ES5 - you must have a Promises/A+ library installed
  * ES6
- Module systems
  * CommonJS
  * ES6 module system


## Development

### Building

To build the TypeScript source code, you need to have Node.js and npm installed.
After cloning the repository, navigate to the project directory and run:

```bash
npm install
npm run build
```

## License

[MIT](LICENSE)
