# Sunlight and Shadow Analyses

## Team
* Marwan Ait-Addi
* John Samuel
* Gilles Gesquière


## Sunpath tool
You can either run this script from the command line, or import it as a library into your project.
This tool lets you calculate the sunpath for each hour of an interval of years (ex: 1975-2025), from the point of view of a single point on eath. Described by its latitde and longitude. The result is exported in a csv file, with a format compatible with [sunlight](https://github.com/VCityTeam/Sunlight) and [pySunlight](https://github.com/VCityTeam/pySunlight).

### Requirements

* Python 3.12 or higher. 
* The [pysolar](https://docs.pysoldsdar.org/en/latest/#prerequisites-for-use) library for python.

We recommend that you use a virtual environment befor installing dependencies
```bash
python3 -m venv venv 
```

Then activate the virtual environment and install the requirements
```bash
. venv/bin/activate
python3 -m pip install -r src/requirements.txt
```


**Example :**
Calculate sunpath for Lyon between 1975 and 2075 (inclusive)
```bash
python3 src/sunpath.py --latitude 45.75 --longitude 4.85 -s 1975 -e 2075
```

Here is a full list of all options available :
| Arguments             | Description                                                                                                           | Example                                   |
| --------------------- | --------------------------------------------------------------------------------------------------------------------- | ----------------------------------------- |
| --latitude, -la       | Latitude for which to calculate sun position                                                                          | -la 45.75                                 |
| --longitude, -lo      | Latitude for which to calculate sun position                                                                          | -lo 4.85                                  |
| --start-year, -s      | Start year of sun position computation                                                                                | -s 1975                                   |
| --end-year, -e        | End year of sun position computation                                                                                  | -e 2075                                   |
| --filename, -f        | Path to CSV file where you want the results to be stored                                                              | -f sunpath.csv                            |