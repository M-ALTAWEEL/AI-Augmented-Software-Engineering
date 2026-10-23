Processing request of type ListToolsRequest
Processing request of type CallToolRequest
HTTP Request: GET https://raw.githubusercontent.com/mledoze/countries/master/countries.json "HTTP/1.1 200 OK"
Processing request of type CallToolRequest
Processing request of type CallToolRequest
Processing request of type CallToolRequest
Processing request of type CallToolRequest
Processing request of type CallToolRequest
Processing request of type CallToolRequest
## tools/list
- search_countries: params=['query', 'limit']
- get_country_details: params=['name']

## tools/call search_countries {"query": "guinea", "limit": 5}
```json
{
  "name": "Guinea",
  "capital": "Conakry",
  "region": "Africa",
  "population": null
}
{
  "name": "Guinea-Bissau",
  "capital": "Bissau",
  "region": "Africa",
  "population": null
}
{
  "name": "Equatorial Guinea",
  "capital": "Ciudad de la Paz",
  "region": "Africa",
  "population": null
}
{
  "name": "Papua New Guinea",
  "capital": "Port Moresby",
  "region": "Oceania",
  "population": null
}
```

## tools/call get_country_details {"name": "Jordan"}
```json
{
  "name": "Jordan",
  "official_name": "Hashemite Kingdom of Jordan",
  "capital": "Amman",
  "region": "Asia",
  "currencies": [
    {
      "code": "JOD",
      "name": "Jordanian dinar",
      "symbol": "د.ا"
    }
  ],
  "languages": [
    "Arabic"
  ],
  "borders": [
    "IRQ",
    "ISR",
    "PSE",
    "SAU",
    "SYR"
  ],
  "flag_url": "https://flagcdn.com/w320/jo.png",
  "flag_emoji": "🇯🇴",
  "source": "mledoze/countries (no API key set)"
}
```

## tools/call get_country_details {"name": "Niger"}
```json
{
  "name": "Niger",
  "official_name": "Republic of Niger",
  "capital": "Niamey",
  "region": "Africa",
  "currencies": [
    {
      "code": "XOF",
      "name": "West African CFA franc",
      "symbol": "Fr"
    }
  ],
  "languages": [
    "French"
  ],
  "borders": [
    "DZA",
    "BEN",
    "BFA",
    "TCD",
    "LBY",
    "MLI",
    "NGA"
  ],
  "flag_url": "https://flagcdn.com/w320/ne.png",
  "flag_emoji": "🇳🇪",
  "source": "mledoze/countries (no API key set)",
  "other_matches": [
    "Nigeria"
  ]
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
  "error": "no country found matching 'Atlantis'; try search_countries to find the exact name",
  "error_type": "not_found"
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
