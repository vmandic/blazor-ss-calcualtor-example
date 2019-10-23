# A blazor calculator example

Project uses .NET Core SDK version: 3.0.100-preview6-012264

## About

A Blazor server-side example with a simple summation calculator component added.

## How to use

- install the .NET Core SDK
- ensure a dev certificate is installed on your system with `dotnet dev-certs https --trust`
- navigate inside the project dir and start the application with `dotnet run`

## HTTP2 is disabled

HTTP2 is by default enabled on the Kestrel server. Due to strange issues with HTTP2 and SSL and Blazor and web-kit based browser (ERR_HTTP2_INADEQUATE_TRANSPORT_SECURITY). 

The HTTP2 is explictly disabled via additional appsetings.json settings with:

```json
  "Kestrel": {
    "EndpointDefaults": {
      "Protocols": "Http1"
    }
  }
```
