# Standardize Country Code

This project helps social science research standardize country codes in multinational research. We follow [ISO 3166-1](https://www.iso.org/iso-3166-country-codes.html) to standardize country identifiers. This list does not take any political or religious conflict into account.

Just in case you are interested in similar data tools, I also constructed:
- [Standardized Security Code](https://github.com/Wenzhi-Ding/Std_Security_Code)
- [Fama French Industry to SIC Link](https://github.com/Wenzhi-Ding/FamaFrenchIndustry)

Please star the projects if you feel it is useful! Many thanks for your appreciation and support!


The list is now cross-sectional, and I would like to develop it into a panel.

Please feel free to contribute if you find any uncovered or wrong country name/number/code. You can either use a pull request or email me at wenzhi.ding@polyu.edu.hk.

- **CountryName**: This dataset is the link table between country names and ISO 3166-1 Alpha-3 code.
- CountryNumber: This dataset is the link table between the ISO 3166-1 Numeric code and ISO 3166-1 Alpha-3 code.
- CountryISO2: This dataset is the link table between the ISO 3166-1 Alpha-2 code and ISO 3166-1 Alpha-3 code.

P.S. I have made some personal adjustments to keep the keys unique in each table. For example, Zaire and Congo share the numeric code 180 but with different alpha codes (ZR, ZAR, CD, COD). I only keep the present regime (180, CD, COD).

## How to Use

You can get the most updated country code link table version in the following ways:

### Python

```python
import pandas as pd

df = pd.read_csv('https://raw.githubusercontent.com/Wenzhi-Ding/StdCountryCode/main/CountryName.csv', encoding='utf-8')  # Please use UTF-8 encoding.
```

### Stata

```stata
import delimited "https://raw.githubusercontent.com/Wenzhi-Ding/StdCountryCode/main/CountryName.csv", clear

rename (Ctry_Name Ctry_ISO3) ([your country name] [your country code])

save "${some_path}CountryName.dta", replace
```


## References

1. [Country Codes Collection (iso.org)](https://www.iso.org/obp/ui/#iso:pub:PUB500001:en)
2. [Country Codes (worldbank.org)](https://wits.worldbank.org/wits/wits/witshelp/content/codes/country_codes.htm)
3. [ISO 3166-3 - Wikipedia](https://en.wikipedia.org/wiki/ISO_3166-3)

