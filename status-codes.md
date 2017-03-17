---
title: "HTTP Status Codes"
cover: http.jpg
endpoints: 2
categories:
layout: api
---
# HTTP Status Codes

| Code | Status | Description |
| --- | --- | --- |

| Data | Data | Data |
| 200 | OK | The request was processed and returned successfully. Nothing was changed. |
| 201 | Created | The new resource was created successfully |
| 202 | Accepted | The request has been accepted for processing, but the processing has not been completed. The request might or might not eventually be acted upon, as it might be disallowed when processing actually takes place. |
| 204 | No Content | The server has fulfilled the request but does not need to return an entity-body, and might want to return updated metainformation. |
| 400 | Bad Request | Problem with the request, such as a missing, invalid or type mismatched parameter |
| 401 | Unauthorized | The request did not have valid authorization credentials |
| 403 | Forbidden | Private data you are not allowed to access, or you've hit a rate limit. |
| 404 | Not Found | Your URL is wrong, or the requested resource doesn't exist. |
| 500 | Server Error | We call this the "crap code" error. Basically we've got a problem on our side. If this persists please contact support. We log and review all errors but your help often helps us fix it quicker. |
| 503 | Service Unavailable | Our API is down. Please try again. We work hard to make this rare. |