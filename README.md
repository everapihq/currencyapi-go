<p align="center">
<img src="https://app.currencyapi.com/img/logo/currencyapi.png" width="300"/>
</p>

# currencyapi-go: Golang Currency Converter

This package is a Golang wrapper for [currencyapi.com] that aims to make the usage of the API as easy as possible in your project.

## Usage

Initialize the API with your API Key (get one for free at [currencyapi.com]):

```go
currencyapi.Init("YOUR-API-KEY")
```

Afterwards you can make calls to the API like this:

### Status Endpoint

```go
currencyapi.Status()
```

### Currencies Endpoint

```go
currencyapi.Currencies()
```

### Latest Endpoint

```go
currencyapi.Latest({
    "base_currency": "USD",
    "currencies": "EUR"
})
```

### Historical Endpoint

```go
currencyapi.Historical({
    "base_currency": "USD",
    "currencies": "EUR",
	"date": "2022-09-04"
})
```

### Conversion Endpoint *

```go
currencyapi.Convert({
    "base_currency": "USD",
    "currencies": "EUR",
	"date": "2022-09-04",
	"value": "1"
})
```

### Range Endpoint *

```go
currencyapi.Range({
    "base_currency": "USD",
    "currencies": "EUR",
	"datetime_start": "2022-09-01T23:59:59Z",
	"datetime_end": "2022-09-03T23:59:59Z",
	"accuracy": "day"
})
```

(*) Requires paid subscription

Find out more about our endpoints, parameters and response data structure in the [docs]

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[docs]: https://currencyapi.com/docs
[currencyapi.com]: https://currencyapi.com
