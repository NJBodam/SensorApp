

# Sensor Data Logger
A command-line Python script for recording, managing, and persisting sensor measurement data. It handles file I/O, data validation, and automatically calculates the timestamp for the next measurement based on a defined time step.

## Features* **Data Persistence:** Load existing sensor data from a `.txt` file or save new entries to a file.
* **Measurement Tracking:** Define sensor parameters (name, unit, time step) and continuously log new values.
* **Time Calculation:** Automatically calculates the date and time of the **next** scheduled measurement.
* **Robust Validation:** Ensures user inputs for dates, times, integers, and float measurements are correctly formatted.

## Getting Started###PrerequisitesYou need **Python 3.x** installed to run this script.

###Usage1. Save the code as `sensor_logger.py`.
2. Run the script from your terminal:
```bash
python sensor_logger.py

```


3. Follow the prompts:
* The script will first ask if you want to **read data from a file** to continue logging existing records.
* If no file is read, you will be prompted to set the initial sensor details (name, unit, and time step).
* The script will then enter a loop, asking for the measured value at the calculated next time slot.
* When finished, you will be asked if you want to **store all accumulated data** in a new output file.



## How Data is StoredThe core data is stored in a list of tuples (`sensorlist`), following this structure for each entry:

```
(id, sensor_name, unit, time_step, year, month, day, hour, minute, measured_value)

```

## Key Functions| Function | Purpose |
| --- | --- |
| `get_file()` | Reads data from a specified input file. |
| `write_output_file()` | Writes all recorded data to a new output file. |
| `is_float()`, `is_date()`, etc. | Validates user input to ensure correct data types and formats. |
| `next_measurement()` | Calculates the date and time for the subsequent reading based on the configured time step. |



