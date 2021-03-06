---
swagger: "2.0"
x-collection-name: eBay
x-complete: 0
info:
  title: Ebay Add Order Order Shipping Fulfillment
  description: 'When you group an order''s line items into one or more packages, each
    package requires a corresponding plan for handling, addressing, and shipping;
    this is a shipping fulfillment. For each package, execute this call once to generate
    a shipping fulfillment associated with that package. Note: A single line item
    in an order can consist of multiple units of a purchased item, and one unit can
    consist of multiple parts or components. Although these components might be provided
    by the manufacturer in separate packaging, the seller must include all components
    of a given line item in the same package.Before using this call for a given package,
    you must determine which line items are in the package. If the package has been
    shipped, you should provide the date of shipment in the request. If not provided,
    it will default to the current date and time.'
  contact:
    name: eBay Inc.
  version: 1.0.0
host: api.ebay.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /order/{orderId}/shipping_fulfillment:
    get:
      summary: Get Order Order Shipping Fulfillment
      description: Use this call to retrieve the contents of all fulfillments currently
        defined for a specified order based on the order's unique identifier, orderId.
        This value is returned in the getOrders call's members.orderId field when
        you search for orders by creation date or shipment status.
      operationId: getShippingFulfillments
      x-api-path-slug: orderorderidshipping-fulfillment-get
      parameters:
      - in: path
        name: orderId
        description: The unique identifier of the order
      responses:
        200:
          description: OK
      tags:
      - Auctions
      - Order
      - Order
      - Shipping
      - Fulfillment
    post:
      summary: Add Order Order Shipping Fulfillment
      description: 'When you group an order''s line items into one or more packages,
        each package requires a corresponding plan for handling, addressing, and shipping;
        this is a shipping fulfillment. For each package, execute this call once to
        generate a shipping fulfillment associated with that package. Note: A single
        line item in an order can consist of multiple units of a purchased item, and
        one unit can consist of multiple parts or components. Although these components
        might be provided by the manufacturer in separate packaging, the seller must
        include all components of a given line item in the same package.Before using
        this call for a given package, you must determine which line items are in
        the package. If the package has been shipped, you should provide the date
        of shipment in the request. If not provided, it will default to the current
        date and time.'
      operationId: createShippingFulfillment
      x-api-path-slug: orderorderidshipping-fulfillment-post
      parameters:
      - in: body
        name: body
        description: fulfillment payload
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: orderId
        description: The unique identifier of the order
      responses:
        200:
          description: OK
      tags:
      - Auctions
      - Order
      - Order
      - Shipping
      - Fulfillment
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---