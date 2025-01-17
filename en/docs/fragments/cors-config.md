SAML2 POST Binding requires CORS configs set up. Before configuring the service provider, make sure you add the following configurations to the `<IS_HOME>/repository/conf/deployment.toml` file to allow HTTP POST requests. 

```toml
[cors]
allow_generic_http_requests = true
allow_any_origin = false
allowed_origins = [
    "http://localhost:8080"
]
allow_subdomains = false
supported_methods = [
    "GET",
    "POST",
    "HEAD",
    "OPTIONS"
]
support_any_header = true
supported_headers = []
exposed_headers = []
supports_credentials = true
max_age = 3600
tag_requests = false
```

