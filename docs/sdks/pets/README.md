# Pets
(*pets*)

### Available Operations

* [create_pets](#create_pets) - Create a pet
* [list_pets](#list_pets) - List all pets
* [show_pet_by_id](#show_pet_by_id) - Info for a specific pet

## create_pets

Create a pet

### Example Usage

```python
import test

s = test.Test()


res = s.pets.create_pets()

if res.status_code == 200:
    # handle response
    pass
```


### Response

**[operations.CreatePetsResponse](../../models/operations/createpetsresponse.md)**
### Errors

| Error Object    | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4x-5xx          | */*             |

## list_pets

List all pets

### Example Usage

```python
import test
from test.models import operations

s = test.Test()

req = operations.ListPetsRequest()

res = s.pets.list_pets(req)

if res.pets is not None:
    # handle response
    pass
```

### Parameters

| Parameter                                                                | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `request`                                                                | [operations.ListPetsRequest](../../models/operations/listpetsrequest.md) | :heavy_check_mark:                                                       | The request object to use for the request.                               |


### Response

**[operations.ListPetsResponse](../../models/operations/listpetsresponse.md)**
### Errors

| Error Object    | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4x-5xx          | */*             |

## show_pet_by_id

Info for a specific pet

### Example Usage

```python
import test
from test.models import operations

s = test.Test()

req = operations.ShowPetByIDRequest(
    pet_id='<value>',
)

res = s.pets.show_pet_by_id(req)

if res.pet is not None:
    # handle response
    pass
```

### Parameters

| Parameter                                                                      | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `request`                                                                      | [operations.ShowPetByIDRequest](../../models/operations/showpetbyidrequest.md) | :heavy_check_mark:                                                             | The request object to use for the request.                                     |


### Response

**[operations.ShowPetByIDResponse](../../models/operations/showpetbyidresponse.md)**
### Errors

| Error Object    | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4x-5xx          | */*             |
