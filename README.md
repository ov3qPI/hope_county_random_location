# random_hope_county_location
Generates a random location from the game Far Cry 5, either from a specific region or from the entire set of locations available in the game.

## Features
- Generate a random location from any of the three main regions: **Henbane**, **Holland**, or **Whitetail**.
- Specify a region to get a random location from that specific area.
- If no region is specified, a location is selected randomly from all available locations.
- Joseph and Dutch's islands were excluded from the set.

## Requirements
- Python 3.x

## Usage
To run the script, use the following command:

```sh
python fc5_location_generator.py [-r REGION]
```

### Arguments
- `-r`, `--region`: Optional argument to specify a region. Can be one of:
  - `Henbane`
  - `Holland`
  - `Whitetail`

If no region is specified, the script will generate a location from all available regions.

### Examples
- Generate a location from any region:
  ```sh
  python fc5_location_generator.py
  ```
- Generate a location specifically from the **Henbane** region:
  ```sh
  python fc5_location_generator.py -r Henbane
  ```

## Code Structure
- **regions**: A dictionary that contains lists of locations, categorized by the three main regions of Far Cry 5.
- **generate_location(region=None)**: Function that returns a random location based on the provided region.
- **main()**: Entry point of the script, which handles argument parsing and calls `generate_location()`.
