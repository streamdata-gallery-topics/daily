---
swagger: "2.0"
x-collection-name: Auth0
x-complete: 1
info:
  title: Auth0 Stats API
  version: v1
host: login.auth0.com
basePath: /stats
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v2/stats/daily:
    get:
      summary: Get Daily Stats
      description: Gets the daily stats for a particular period.
      operationId: get_daily
      x-api-path-slug: apiv2statsdaily-get
      parameters:
      - in: query
        name: from
        description: The first day of the period (inclusive) in YYYYMMDD format
      - in: query
        name: to
        description: The last day of the period (inclusive) in YYYYMMDD format
      responses:
        200:
          description: OK
      tags:
      - Stats
      - Daily
---