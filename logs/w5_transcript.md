Processing request of type ListToolsRequest
Processing request of type CallToolRequest
HTTP Request: GET https://restcountries.com/v3.1/name/guinea?fields=name%2Ccapital%2Cregion%2Cpopulation "HTTP/1.1 301 Moved Permanently"
Processing request of type CallToolRequest
HTTP Request: GET https://restcountries.com/v3.1/name/Jordan?fields=name%2Ccapital%2Cregion%2Ccurrencies%2Clanguages%2Cborders%2Cflags%2Cflag&fullText=true "HTTP/1.1 301 Moved Permanently"
Processing request of type CallToolRequest
HTTP Request: GET https://restcountries.com/v3.1/name/Niger?fields=name%2Ccapital%2Cregion%2Ccurrencies%2Clanguages%2Cborders%2Cflags%2Cflag&fullText=true "HTTP/1.1 301 Moved Permanently"
Processing request of type CallToolRequest
Processing request of type CallToolRequest
HTTP Request: GET https://restcountries.com/v3.1/name/Atlantis?fields=name%2Ccapital%2Cregion%2Ccurrencies%2Clanguages%2Cborders%2Cflags%2Cflag&fullText=true "HTTP/1.1 301 Moved Permanently"
Processing request of type CallToolRequest
Processing request of type CallToolRequest
## tools/list
- search_countries: params=['query', 'limit']
- get_country_details: params=['name']

## tools/call search_countries {"query": "guinea", "limit": 5}
```json
{
  "error": "REST Countries returned a response that is not JSON",
  "error_type": "bad_response"
}
```

## tools/call get_country_details {"name": "Jordan"}
```json
{
  "error": "REST Countries returned a response that is not JSON",
  "error_type": "bad_response"
}
```

## tools/call get_country_details {"name": "Niger"}
```json
{
  "error": "REST Countries returned a response that is not JSON",
  "error_type": "bad_response"
}
```

## tools/call get_country_details {"name": "12345"}
```json
{
  "error": "name may only contain letters, spaces and . ' - ( ) , &",
  "error_type": "invalid_input"
}
```

## tools/call get_country_details {"name": "Atlantis"}
```json
{
  "error": "REST Countries returned a response that is not JSON",
  "error_type": "bad_response"
}
```

## tools/call search_countries {"query": "   "}
```json
{
  "error": "query must not be empty",
  "error_type": "invalid_input"
}
```

## tools/call search_countries {"query": "jor", "limit": 99}
```json
{
  "error": "limit must be an integer between 1 and 25",
  "error_type": "invalid_input"
}
```
