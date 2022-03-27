# Structure

```
{
  # The base currency to trade against other wanted currencies:
  "fromCurrency" : "USD",

  # List of other wanted currencies to trade against fromCurrency:
  "toCurrencies" : [
      "AUD",
      "CAD",
      "MXN",
      "EUR",
      "GBP"
  ],

  # Traded pairs (fromCurrency, toCurrencies) to monitor:
  "trades": [
    {
      # toCurrency
      "currency": "AUD",

      "signals": {
        # To sell fromCurrency at this rate:
        "sell": 1.44927,

        # To buy back when fromCurrency reaches this rate against toCurrency:
        "buy": 1.35169,

        # The first resistance above the buy signal
        "buyResistance1": 1.34228,

        # The second resistance above the buy signal
        "buyResistance2": 1.33333,

        # The third resistance above the buy signal
        "buyResistance3": 1.28205,
      }
    }
  ]
}
```

# Notes:

- If trade signal reaches 2nd resistance but only to fall back to a midpoint of
  1st and 2nd resistances then review trend and tune the buy signals.

- If trade signal reaches 3rd resistance but only to fall back to a midpoint of
  2nd and 3rd resistances then seriously consider buy back fromCurrency.
