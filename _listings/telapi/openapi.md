swagger: "2.0"
x-collection-name: TelAPI
x-complete: 1
info:
  title: TelAPI
  description: telapi-is-a-rest-api--what-that-means-for-you-is-that-interacting-with-telapi-to-perform-all-of-your-telephony-needs-is-almost-as-simple-as-visiting-a-website--deeper-knowledge-regarding-rest-is-useful-when-developing-with-telapi-but-definitely-not-required--we-aim-to-provide-all-of-the-information-needed-for-working-with-our-rest-api-throughout-its-documentation-provided-here-so-even-if-you-are-new-to-rest-telapi-will-still-be-a-pleasure-to-use-
  termsOfService: http://www.telapi.com/legal/tos
  version: v2
host: api.telapi.com
basePath: v2/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/hotel/v0/hotels/{hotelId}/rateplans/{rateplanCode}/rates:
    get:
      summary: Get the setup of the daily rates for a specific rateplan and a defined
        timeperiod.
      description: "With this call you can read the daily rates setup including the
        cancellation policy and minimum guarantee per day for the\r\n            specified
        rateplan. You can specify a timeperiod to read the daily rates for. The rateplan
        needs to be active for at least\r\n            one business day in the defined
        time period and have rates loaded."
      operationId: RatePlans_GetRates
      x-api-path-slug: apihotelv0hotelshotelidrateplansrateplancoderates-get
      parameters:
      - in: header
        name: App-Id
        description: Application identifier
      - in: header
        name: App-Key
        description: Application key
      - in: query
        name: expand
        description: You can expand the supplements per room type on demand
      - in: query
        name: from
        description: Defines the last business day you would like to get rates for
      - in: path
        name: hotelId
        description: The hotel id the rateplan belongs to
      - in: query
        name: inlinecount
        description: Return total number of items for a given filter criteria
      - in: path
        name: rateplanCode
        description: The code of the rateplan you want to see details for
      - in: query
        name: skip
        description: Amount of items to skip
      - in: query
        name: to
        description: Defines the first business day you would like to get rates for
      - in: query
        name: top
        description: Amount of items to select
      responses:
        200:
          description: OK
      tags:
      - Setup
      - Of
      - Daily
      - Ratesa
      - Specific
      - Rateplan
      - Defined
      - Timeperiod
  /api/hotel/v0/hotels/{hotelId}/rateplans/{rateplanCode}/rates/$count:
    get:
      summary: Get the count of all active and loaded daily rates for the defined
        rateplan in a specified time period.
      description: Get the count of all active and loaded daily rates for the defined
        rateplan in a specified time period..
      operationId: RatePlans_GetRatesCount
      x-api-path-slug: apihotelv0hotelshotelidrateplansrateplancoderatescount-get
      parameters:
      - in: header
        name: App-Id
        description: Application identifier
      - in: header
        name: App-Key
        description: Application key
      - in: query
        name: from
        description: Defines the last business day you would like to get rates for
      - in: path
        name: hotelId
        description: The hotel id the rateplan belongs to
      - in: path
        name: rateplanCode
        description: The code of the rateplan you want to count daily rates for
      - in: query
        name: to
        description: Defines the first business day you would like to get rates for
      responses:
        200:
          description: OK
      tags:
      - Count
      - Of
      - ""
      - Active
      - Loaded
      - Daily
      - Ratesthe
      - Defined
      - Rateplan
      - In
      - Specified
      - Time
      - Period
  /api/hotel/v0/hotels/{hotelId}/rateplans/{rateplanCode}/rates/{businessDay}:
    get:
      summary: Get the setup of a daily rate for a specific business day and rateplan.
      description: Read the setup of the daily rate for the defined rateplan for that
        specific business day.
      operationId: RatePlans_GetRate
      x-api-path-slug: apihotelv0hotelshotelidrateplansrateplancoderatesbusinessday-get
      parameters:
      - in: header
        name: App-Id
        description: Application identifier
      - in: header
        name: App-Key
        description: Application key
      - in: path
        name: businessDay
        description: The business day you want to get the rate setup for
      - in: path
        name: hotelId
        description: The hotel id the rateplan belongs to
      - in: path
        name: rateplanCode
        description: The code of the rateplan you want to see details for
      responses:
        200:
          description: OK
      tags:
      - Setup
      - Of
      - Daily
      - Ratea
      - Specific
      - Business
      - Day
      - Rateplan