---
swagger: "2.0"
x-collection-name: WebTRIS
x-complete: 0
info:
  title: WebTRIS Traffic Flow API Gets the daily report.
  version: 1.0.0
  description: Gets the daily report..
host: webtris.highwaysengland.co.uk
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v{version}/reports/{report_type}:
    get:
      summary: Gets the daily report.
      description: Gets the daily report..
      operationId: Reports_Index
      x-api-path-slug: vversionreportsreport-type-get
      parameters:
      - in: query
        name: end_date
        description: The end date of the report in the format ddmmyyyy (i
      - in: query
        name: page
        description: The page offset to return
      - in: query
        name: page_size
        description: The number of rows to return
      - in: query
        name: reportSubTypeId
      - in: path
        name: report_type
        description: Report Type Id (i
      - in: query
        name: sites
        description: Comma separated list of site Ids
      - in: query
        name: start_date
        description: The start date of the report in the format ddmmyyyy (i
      - in: path
        name: version
      responses:
        200:
          description: OK
      tags:
      - S
      - Daily
      - Report
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