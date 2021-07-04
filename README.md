# Standardize Country Code

This project is to help social science research to standardize country code in multinational research. We follow [ISO 3166-1](https://www.iso.org/iso-3166-country-codes.html) to standardize country identifiers. This list does not take any political or religious conflict into account.

The list is now cross-sectional and we have a plan to develop it into a panel data.

Please feel free to contribute if you find any uncovered country name/number/code. If you are not familiar with GitHub, you can send your request to this [email](mailto:wenzhi.ding@connect.hku.hk).

- **CountryName**: This dataset is the link table between country names and ISO 3166-1 Alpha-3 code. (This one is updated more frequently. You are advised to use this file in priority.)
- CountryNumber: This dataset is the link table between ISO 3166-1 Numeric code and ISO 3166-1 Alpha-3 code.
- CountryISO2: This dataset is the link table between ISO 3166-1 Alpha-2 code to ISO 3166-1 Alpha-3 code.

## Use in Python

```python
import pandas as pd

df = pd.read_csv('https://raw.githubusercontent.com/Wenzhi-Ding/StdCountryCode/main/CountryName.csv', encoding='latin-1')
```

In this way, you can always get the most updated version of country code link tables.

# References

1. [Country Codes Collection (iso.org)](https://www.iso.org/obp/ui/#iso:pub:PUB500001:en)
2. [Country Codes (worldbank.org)](https://wits.worldbank.org/wits/wits/witshelp/content/codes/country_codes.htm)
3. [ISO 3166-3 - Wikipedia](https://en.wikipedia.org/wiki/ISO_3166-3)

