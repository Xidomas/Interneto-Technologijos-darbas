# Unofficial MAL Manga Client

## Description
- [ ] My system will allow users to use mal  functions using android app.

## Entity definition
Manga - entity
characters -
news	
pictures	
stats	
forum	
moreinfo	
reviews	Page number (integer)
recommendations	
userupdates	Page number (integer)





- [ ] Define the entity ("object" that will be manipulated) of WEB system
- [ ] Entity should have a name
- [ ] Entity should have 3 mandatory attributes:
    - [ ] ID - depending on specific service this could be a number or string
    - [ ] Creation date - (if applicable for specific service) ISO 8601 format date string
    - [ ] Modification date - (if applicable for specific service) ISO 8601 format date string
- [ ] Entity should have at least 5 custom attributes
    - [ ] Each attribute should have a type defined: number, string, ISO 8601 date string, boolean, object, array or other
    - [ ] Each attribute should have restrictions defined: list of constants, or number range, or string length, or string format, or object schema, or array schema or other. For example, you can use `joi` language to define restrictions: https://github.com/hapijs/joi/blob/v13.1.2/API.md

## API definition

Get /api/1/userid/mangalist

- [ ] Define specific service (konkrečios paslaugos) API methods that WEB system is going to use
- [ ] Optionally define additional API methods that WEB system is going to expose
- [ ] API should have at least 4 methods
    - [ ] A method to return entity by ID. Should not have request body
    - [ ] A method to return multiple entities (Array) by ID. This method should support at least one header value to:
        - [ ] Return only entities that match pattern in one of its attributes
        - [ ] Return 10 entities starting provided index
        - [ ] Return sorted entities by one of its attributes (both ascending and descending)
        - [ ] Other (should be approved by Product Owner (PO))
    - [ ] A method to remove entity by ID. Returns removed entity. Should not have request body
    - [ ] A method to update entity by ID. Accepts entity to update and returns updated entity
- [ ] Each method should have HTTP method defined
- [ ] Each method should have URI defined (use {id} as entity ID placeholder)
- [ ] Should return all 4xx errors in unified format. Define format using `joi` language
- [ ] Should return all 5xx errors in unified format. Define format using `joi` language

## UI definition
- [ ] Define the structure of how visually the WEB system is going to look like
- [ ] Should have at least one view defined with https://wireframe.cc (or other wireframe tool):
- [ ] The view should have a title
- [ ] The view should have a description of a service provided by web system
- [ ] The view should include at least 2 UI components:
    - [ ] A component to display multiple entities with all their attribute values visible. It should be posible to remove and edit selected entity.
        - [ ] Depending on chosen header of API method that returns multiple entities, it should be posible to select specific 10 entities starting index, sort entities by attribute, filter entities by attribute pattern, or other (should be approved by Product Owner (PO))
    - [ ] A component to create a new entity/edit existing entity. It should be posbile to create new entity and edit selected entity
        - [ ] Each attribute should have a dedicated editor field: text box for string or number, checkbox or radio buttons for boolean, date picker for date, etc.



===================================================================================================================================

Currency exchange turbo viewer
Description
My system will allow users to store currency pairs for certain amount and see its exchang value in real time.

Entity definition
Currency Pair

id - SHA-2 hash
creationDate - ISO 8601 (i.e.: 2010-01-01T00:01:12.123Z+03:00)
modificationDate - ISO 8601
currencyFrom - string, 3 char length, upper case
currencyTo - string, 3 char length, upper case
amount - number, min - 1, max - 1 000 000
userId - SHA-2 hash
API definition
GET /api/1/user/:userId/currencyPairs - will return all crc pairs for user :userId in entity definition format

400 - { error: 'invalid user ID' } POST /api/1/user/:userId/currencyPairs - will allow to add new currency pair for user :userId in definition format

400 - { error: 'invalid user ID' }

400 - { error: [{ error: 'currencyFrom is invalid crc' }, { error: 'currencyTo is invalid crc' }, { error: 'invalid amount' }]} GET /api/1/user/:userId/currencyPairs/:id - will return currency pair exchange rate in format: { date: ISO 8601, rate: float number }. Rate will be retrieved from external public API.

400 - { error: 'invalid user ID' }

400 - { error: 'invalid crc ID' } DELETE /api/1/user/:userId/currencyPairs/:id - will delete currency pair with ID :id

400 - { error: 'invalid user ID' }

400 - { error: 'invalid crc ID' }

404 - { error: 'REST service is not found' }

500 - { error: 'retry' }, { error: 'server error' }

UI definition
https://wireframe.cc/vR9Euf


https://github.com/ExampleJenkinsOrg/web-system-template
