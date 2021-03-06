swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 1
info:
  title: plentymarkets REST-API
  description: the-plentymarkets-rest-api-expands-the-functionality-of-the-plentymarkets-cms-and-allows-access-to-resources-i-e--data-records-via-unique-uri-paths
  contact:
    name: plentymarkets
    url: https://forum.plentymarkets.com/c/rest-api
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/items/manufacturers:
    get:
      summary: List manufacturers
      description: |-
        Lists all manufacturers in the system.

        Display a listing of the resource.
      operationId: getRestItemsManufacturers
      x-api-path-slug: restitemsmanufacturers-get
      parameters:
      - in: query
        name: name
        description: Filter restricts the list of results to records with specified
          name
      - in: query
        name: updatedAt
        description: Filter restricts the list of results to records updated after
          the specified date
      responses:
        200:
          description: OK
      tags:
      - List
      - Manufacturers
    post:
      summary: Create a manufacturer
      description: Creates a manufacturer.
      operationId: postRestItemsManufacturers
      x-api-path-slug: restitemsmanufacturers-post
      responses:
        200:
          description: OK
      tags:
      - Manufacturer
  /rest/items/manufacturers/{id}:
    delete:
      summary: Delete a manufacturer
      description: Deletes a manufacturer. The ID of the manufacturer must be specified.
      operationId: deleteRestItemsManufacturers
      x-api-path-slug: restitemsmanufacturersid-delete
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Manufacturer
    get:
      summary: Get a manufacturer
      description: Gets a manufacturer. The ID of the manufacturer must be specified.
      operationId: getRestItemsManufacturers
      x-api-path-slug: restitemsmanufacturersid-get
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Manufacturer
    put:
      summary: Update a manufacturer
      description: Updates a manufacturer. The ID of the manufacturer must be specified.
      operationId: putRestItemsManufacturers
      x-api-path-slug: restitemsmanufacturersid-put
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Manufacturer