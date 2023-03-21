# Minimal Document Structure

**Which fields in the root object are mandatory?**

Only two fields are mandatory in an OpenAPI Object:

* openapi
* info

Aditionally, at least one of `paths`, `component` and `webhooks` is required.

* `openapi` (string): This indicates the version of the OAS this document is using.
* `info` (Info Object): This provides general information about the API but the the only mandatory fields are `title` and `version`.
  * `title` (string): A human-readable name for the API.
  * `version` (string): Indicates the version **of the API document**
* `paths` (Path Object): This describes all the **endpoints** of the API, including their parameters and all possible server responses.

Minimal OpenAPI document example:

```yaml
openapi: 3.1.0
info:
  title: A minimal OpenAPI document
  version: 0.0.1
paths: {} # No endpoints defined
```