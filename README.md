# Warehouse tools

Small Python utilities for warehouse order and shipping workflows.

Run the tests with `python3 -m unittest discover -s tests -v`.

## Shipping

`shipping_quote(weight_kg, zone, service="standard")` returns a shipping quote
in dollars.

| Parameter | Values | Notes |
|-----------|--------|-------|
| `weight_kg` | positive float | parcel weight |
| `zone` | `"local"`, `"regional"` | delivery zone |
| `service` | `"standard"` (default), `"express"` | express adds $7 flat |

The CLI accepts the same options:

```
python -m warehouse.cli 2.5 local                     # standard
python -m warehouse.cli 2.5 local --service express   # express
```
