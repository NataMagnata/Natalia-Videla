# Solar Energy Analysis Project

This project contains a series of Jupyter notebooks for analyzing solar energy potential and economic feasibility in different locations. The analysis includes both Photovoltaic (PV) and Concentrated Solar Power (CSP) systems.

## Project Structure

The project consists of the following notebooks:

1. `final_limpiezas.ipynb`: Data cleaning and processing
   - Processes weather data from CSV files
   - Converts data to PVWatts v8 format
   - Handles multiple locations (Chile, Russia, China)
   - Calculates solar irradiance statistics

2. `final_simulacion_pv.ipynb`: Photovoltaic system simulation
   - Simulates PV system performance
   - Analyzes energy production

3. `final_simulacion_csp.ipynb`: Concentrated Solar Power simulation
   - Simulates CSP system performance
   - Analyzes thermal energy production

4. `final_lcoe.ipynb`: Levelized Cost of Energy analysis
   - Calculates LCOE for different scenarios
   - Economic feasibility analysis

5. `final_analisis_sensibilidad.ipynb`: Sensitivity analysis
   - Analyzes how different parameters affect system performance
   - Evaluates economic sensitivity

## Requirements

- Python 3.10 or higher
- Jupyter Notebook
- Required Python packages:
  - pandas
  - numpy
  - matplotlib
  - pvlib (for PV simulations)
  - SAM (System Advisor Model) for CSP simulations

## Installation

1. Clone this repository:
```bash
git clone [repository-url]
cd [repository-name]
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

## Usage

1. Start Jupyter Notebook:
```bash
jupyter notebook
```

2. Open the notebooks in the following order:
   - First run `final_limpiezas.ipynb` to process the weather data
   - Then run either `final_simulacion_pv.ipynb` or `final_simulacion_csp.ipynb` depending on your needs
   - Finally, run `final_lcoe.ipynb` and `final_analisis_sensibilidad.ipynb` for economic analysis

## Input Data

The project uses weather data in CSV format with the following naming convention:
- `tmy_[latitude]_[longitude]_[start_year]_[end_year].csv`

Example: `tmy_-38.320_-71.960_2005_2023.csv`

The input data should contain the following columns:
- time(UTC)
- T2m (Temperature)
- RH (Relative Humidity)
- G(h) (Global Horizontal Irradiance)
- Gb(n) (Direct Normal Irradiance)
- Gd(h) (Diffuse Horizontal Irradiance)
- WS10m (Wind Speed)
- WD10m (Wind Direction)
- SP (Surface Pressure)

## Output

The processed data will be saved in PVWatts v8 format with the following naming convention:
- `[original_filename]_pvwatts_final.csv`

## Contributing

Feel free to submit issues and enhancement requests.

## License

[Add your license information here] 