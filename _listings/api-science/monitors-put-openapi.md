---
swagger: "2.0"
x-collection-name: API Science
x-complete: 0
info:
  title: API Science Apply Actions to Multiple Monitors
  version: 1.0.0
  description: Apply Actions to Multiple Monitors
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /monitors:
    get:
      summary: Get All Monitors
      description: Marks message as read.
      operationId: getAllMonitors
      x-api-path-slug: monitors-get
      parameters:
      - in: header
        name: Authorization
        description: Your API key must be included in all API requests to the server
          in an Authorization HTTP header
      - in: query
        name: tags
        description: Optionally filter monitors by tags
      responses:
        200:
          description: OK
      tags:
      - Monitors
    post:
      summary: Create a Monitor
      description: Create a Monitor
      operationId: createMonitor
      x-api-path-slug: monitors-post
      parameters:
      - in: formData
        name: active
        description: This flag determines whether the monitor is either running or
          paused
      - in: formData
        name: frequency
        description: The frequency that you want this monitor to be run at
      - in: formData
        name: name
        description: The name of the monitor
      - in: formData
        name: templates
        description: An array of template objects to be created
      responses:
        200:
          description: OK
      tags:
      - Monitors
    put:
      summary: Apply Actions to Multiple Monitors
      description: Apply Actions to Multiple Monitors
      operationId: applyActionsToMultipleMonitors
      x-api-path-slug: monitors-put
      parameters:
      - in: path
        name: tags
        description: Optionally filter monitors by tags
      responses:
        200:
          description: OK
      tags:
      - Monitors
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