---
swagger: "2.0"
x-collection-name: Microsoft Graph
x-complete: 0
info:
  title: Microsoft Graph Range Fill Clear
  description: 'RangeFill: clear Resets the range background.'
  version: 1.0.0
host: graph.microsoft.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /workbook/names(&lt;name&gt;)/range/format/fill/clear:
    post:
      summary: Range Fill Clear
      description: 'RangeFill: clear Resets the range background.'
      operationId: RangeFill:Clear
      x-api-path-slug: workbooknamesltnamegtrangeformatfillclear-post
      parameters:
      - in: header
        name: Authorization
        description: Bearer
      responses:
        200:
          description: OK
      tags:
      - Range
      - Fill
      - Clear
  /workbook/worksheets(&lt;id|name&gt;)/range(&lt;address&gt;)/format/fill/clear:
    post:
      summary: Range Fill Clear
      description: 'RangeFill: clear Resets the range background.'
      operationId: RangeFill:Clear
      x-api-path-slug: workbookworksheetsltidnamegtrangeltaddressgtformatfillclear-post
      parameters:
      - in: header
        name: Authorization
        description: Bearer
      responses:
        200:
          description: OK
      tags:
      - Range
      - Fill
      - Clear
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