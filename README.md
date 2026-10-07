# Maji Ndogo Digital Twin: Teaching a Farm Model to Make Decisions

**Built for:** hiring managers and technical reviewers

## The problem
Maji Ndogo's Ministry of Agriculture wanted a Digital Twin of its farms: a programmable model that tracks what has been planted, decides when a tractor needs fuel, and keeps a record of every farm's harvest. My task was the logic layer, written in plain Python with no libraries or databases.

## What I built
Eight functions, each solving one farm-management question:
- `fuel_status` classifies a tractor's tank as Empty, Low, OK or Full.
- `count_planted_cells` counts planted cells across a field grid using nested loops.
- `drive_and_plant` drives a tractor down a row and stops at an obstacle.
- `total_horsepower` and `low_fuel_models` summarise the vehicle fleet.
- `revenue_by_crop` prices a whole harvest with a dictionary comprehension.
- `compare_crop_plans` compares two farms' crops using set operations.
- `record_harvest` maintains a nested-dictionary registry of every farm's harvest.

## Bugs I hit along the way
- **A loop that counted one row too many.** 
- **A `KeyError` in the harvest registry.** A new farm had no entry yet, so adding to it failed. The fix was to check whether the farm exists first and create it if not.
- **A function that returned `None`.** I forgot the `return` statement, so the function ran but gave nothing back.



## Results
Every function passes the challenge's test inputs. For example, `total_horsepower` returns 450 for the sample fleet, and `compare_crop_plans` correctly separates shared crops from crops only one farm grows.

## Tools and concepts
Python, conditionals, `while` and `for` loops, list and dictionary comprehensions, sets, nested dictionaries.
