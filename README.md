# SteamDeckApproximator
A Jupyter notebook simplifying estimating date of SteamDeck order email based on Fammy's data.

# Requirements

You may adjust them to your own needs, if you have enough development knowledge.

OS:
* Windows (tested)
* Linux (should work)
* MacOS (should work)

* Visual Studio Code (as a Jupyter client)
    * You may need to install some plugins to Code, it will prompt you
* Python 3.9
* Python packages: `numpy`, `matplotlib`, `pandas`, `requests`

# Usage

Configure the script in the first code block:

```python
# CONFIGURE HERE:

myLocale = "en_US.utf8"            # ** Leave unchanged **
myReserveTime = 1657306697         # Your rtReserveTime
firstEuReserveTime = 1626454800    # This is the date of first email of Steam Deck, will be most likely the same for all regions
myModel = '512GB';                 # Your model: 64GB, 256GB or 512GB only
myRegion = 'UK';                   # Your region: US, UK or EU only
regressionDaysNumber = 7;          # How many days to take for estimation. Pick 3 for the recent trend, 5-7 for more general trend
regressionDegree = 1;              # Degression function. 1 is linear. Leave intact if you don't know what it is.
fammysUrl = 'https://docs.google.com/spreadsheet/ccc?key=1ZaKncig9fce7K0sr1f-E2_sgLH1HuKQ-q3k7clPMOCs&output=csv';  # ** Leave unchanged **
```

Afterwards run all scripts. The notebook automatically downloads the latest version of Fammy's data, so it is generally a fire and forget type of script.
