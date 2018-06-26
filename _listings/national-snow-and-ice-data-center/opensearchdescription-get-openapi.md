---
swagger: "2.0"
x-collection-name: National Snow and Ice Data Center
x-complete: 0
info:
  title: NSIDC Web Service Documentation Index Describes the web interface of NSIDC's
    data search engine
  description: Describes the web interface of NSIDC's data search engine
  version: 1.0.0
host: nsidc.org
basePath: /api/dataset/2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Facets:
    get:
      summary: View the facet information corresponding to a search
      description: In the NSIDC Search and Arctic Data Explorer interfaces, this endpoint
        is used in conjunction with /OpenSearch whenever a user submits a new search.
        Consequently, it has the same parameters as /OpenSearch.
      operationId: facets
      x-api-path-slug: facets-get
      parameters:
      - in: query
        name: count
        description: The number of search results per page desired by the client;
          OpenSearch 1
      - in: query
        name: endDate
        description: The end date in yyyy-mm-dd format
      - in: query
        name: facetFilters
        description: Describes faceted restrictions on the search
      - in: query
        name: searchTerms
        description: URL-encoded keyword or keywords desired by the client; OpenSearch
          1
      - in: query
        name: sortKeys
        description: Sort the results by most relevant (default), smallest or largest
          spatial area, shortest or longest temporal duration, or most recently updated;
          partial implementation of OpenSearch SRU 1
      - in: query
        name: source
        description: Custom parameter for selecting which source to use; the Arctic
          Data Explorer (ADE) uses data aggregated from many sources, including, but
          not limited to, NSIDC
      - in: query
        name: spatial
        description: 4 comma separated values - W, S, E, N; OpenSearch-Geo 1
      - in: query
        name: startDate
        description: The start date in yyyy-mm-dd format
      - in: query
        name: startIndex
        description: First search result desired by the search client; OpenSearch
          1
      responses:
        200:
          description: OK
      tags:
      - Environment
  /OpenSearch:
    get:
      summary: Search documents using the OpenSearch 1.1 Specification
      description: This endpoint uses parameters from the OpenSearch 1.1 specification,
        as well as parameters from the OpenSearch Geo (1.0) and SRU (1.0) extensions.
      operationId: OpenSearch.get
      x-api-path-slug: opensearch-get
      parameters:
      - in: query
        name: count
        description: The number of search results per page desired by the client;
          OpenSearch 1
      - in: query
        name: endDate
        description: The end date in yyyy-mm-dd format
      - in: query
        name: facetFilters
        description: Describes faceted restrictions on the search
      - in: query
        name: searchTerms
        description: URL-encoded keyword or keywords desired by the client; OpenSearch
          1
      - in: query
        name: sortKeys
        description: Sort the results by most relevant (default), smallest or largest
          spatial area, shortest or longest temporal duration, or most recently updated;
          partial implementation of OpenSearch SRU 1
      - in: query
        name: source
        description: Custom parameter for selecting which source to use; the Arctic
          Data Explorer (ADE) uses data aggregated from many sources, including, but
          not limited to, NSIDC
      - in: query
        name: spatial
        description: 4 comma separated values - W, S, E, N; OpenSearch-Geo 1
      - in: query
        name: startDate
        description: The start date in yyyy-mm-dd format
      - in: query
        name: startIndex
        description: First search result desired by the search client; OpenSearch
          1
      responses:
        200:
          description: OK
      tags:
      - Environment
  /OpenSearchDescription:
    get:
      summary: Describes the web interface of NSIDC's data search engine
      description: Describes the web interface of NSIDC's data search engine
      operationId: OpenSearchDescription.get
      x-api-path-slug: opensearchdescription-get
      responses:
        200:
          description: OK
      tags:
      - Environment
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