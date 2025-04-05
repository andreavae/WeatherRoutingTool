# Weather Routing Tool (WRT)
As a first contribution to the Weather Routing Tool (WRT), I implemented a new synthetic ship class called MySyntheticBoat, following the structure of the existing ConstantFuelBoat example. The goal of this contribution is to start becoming familiar with the codebase, and lay the foundation for further work during GSoC 2025.

🛠️ What Has Been Implemented
1. New Ship Class: MySyntheticBoat
Located in: WeatherRoutingTool/ship/ship.py

Inherits from the base Boat class.
Implements the required method get_ship_params.

The fuel_rate is computed synthetically, based on an environmental parameter (specifically: wave height).

The formula used is:  fuel_rate = base_rate + factor * wave_height
where:
base_rate = 0.2 kg/s
factor = 0.05 kg/s per meter of wave height

The ship travels at a constant speed of 5.0 knots.

This provides a basic dynamic consumption model that responds to weather conditions, as required by the code challenge.

2. Minimal Test Setup
To validate the implementation:
The configuration was updated to use the new ship class by setting BOAT_TYPE = "MySyntheticBoat" in configuration.py.

🎯 Next Steps
More advanced work that could be done in GSoC, could be:
- Ship speed optimization
- Improved genetic algorithms
- Development of a general consumption model
- Benchmarking and performance improvements.
