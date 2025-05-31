# 36244

First, read the [Renovate minimal reproduction instructions](https://github.com/renovatebot/renovate/blob/main/docs/development/minimal-reproductions.md).

Then replace the current `h1` with the Renovate Issue/Discussion number.

## Current behavior

Warning

```
Repository problems
These problems occurred while renovating this repository.

Release interceptor failed for "crate"
```

```
WARN: Release interceptor failed for "crate"
{
  "err": {
    "name": "HTTPError",
    "code": "ERR_NON_2XX_3XX_RESPONSE",
    "timings": {
      "start": 1748711239306,
      "socket": 1748711239306,
      "lookup": 1748711239342,
      "connect": 1748711239344,
      "secureConnect": 1748711239350,
      "upload": 1748711239351,
      "response": 1748711239355,
      "end": 1748711239357,
      "phases": {
        "wait": 0,
        "dns": 36,
        "tcp": 2,
        "tls": 6,
        "request": 1,
        "firstByte": 4,
        "download": 2,
        "total": 51
      }
    },
    "message": "Response code 404 (Not Found)",
    "stack": "HTTPError: Response code 404 (Not Found)\n    at Request.<anonymous> (/usr/local/renovate/node_modules/.pnpm/got@11.8.6/node_modules/got/dist/source/as-promise/index.js:118:42)\n    at processTicksAndRejections (node:internal/process/task_queues:105:5)",
    "options": {
      "headers": {
        "user-agent": "RenovateBot/40.33.6 (https://github.com/renovatebot/renovate)",
        "accept": "application/json",
        "accept-encoding": "gzip, deflate, br"
      },
      "url": "https://crates.io/api/v1/crates/serde_yaml/0.9.34",
      "hostType": "crate",
      "username": "",
      "password": "",
      "method": "GET",
      "http2": false
    },
    "response": {
      "statusCode": 404,
      "statusMessage": "Not Found",
      "body": {
        "errors": [
          {
            "detail": "crate `serde_yaml` does not have a version `0.9.34`"
          }
        ]
      },
      "headers": {
        "content-type": "application/json",
        "content-length": "81",
        "connection": "keep-alive",
        "access-control-allow-origin": "*",
        "content-encoding": "br",
        "date": "Sat, 31 May 2025 17:07:12 GMT",
        "nel": "{\"report_to\":\"heroku-nel\",\"response_headers\":[\"Via\"],\"max_age\":3600,\"success_fraction\":0.01,\"failure_fraction\":0.1}",
        "report-to": "{\"group\":\"heroku-nel\",\"endpoints\":[{\"url\":\"https://nel.heroku.com/reports?s=clR5y9BvZCqYzr9KEnDk8HrYp2q02rJFh0%2B1Uzqanes%3D\\u0026sid=af571f24-03ee-46d1-9f90-ab9030c2c74c\\u0026ts=1748711232\"}],\"max_age\":3600}",
        "reporting-endpoints": "heroku-nel=\"https://nel.heroku.com/reports?s=clR5y9BvZCqYzr9KEnDk8HrYp2q02rJFh0%2B1Uzqanes%3D&sid=af571f24-03ee-46d1-9f90-ab9030c2c74c&ts=1748711232\"",
        "server": "Heroku",
        "strict-transport-security": "max-age=31536000; includeSubDomains",
        "via": "1.1 heroku-router, 1.1 309e9e958e8d35f7e17ae8ac267b7dea.cloudfront.net (CloudFront)",
        "vary": "accept-encoding",
        "x-cache": "Error from cloudfront",
        "x-amz-cf-pop": "IAD12-P1",
        "x-amz-cf-id": "B3ipifGo3FYkX_mbB7UB9MOrxuqV1yhd-pNI9Od0tfBjzlmzo38bGQ==",
        "age": "7"
      },
      "httpVersion": "1.1",
      "retryCount": 0
    }
  }
}
```

https://developer.mend.io/github/andrzejressel/renovate-discussion-36244/-/job/a627541e-ecc4-4232-bcea-ebbe2bff6ac7

## Expected behavior

No errors

## Link to the Renovate issue or Discussion

https://github.com/renovatebot/renovate/discussions/36244