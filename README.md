# UK Traffic Accidents - Casualties Dataset (STATS19)
## Overview:
This dataset contains casualty-level records from reported road traffic accidents in the United Kingdom, collected through the official STATS19 system.
Each row represents one individual casualty (injured or killed) involved in a reported traffic collision.
The dataset focuses exclusively on casualties, describing:
- Demographic characteristics of the casualty.
- The role of the casualty in the collision.
- Injury severity and adjusted severity indicators.
- Selected social and spatial attributes.
## Unit of Observation:
- One row  = one casualty (person).
- Multiple casualties may be associated with:
  - The same collision **(collision_index)**.
  - The same vehicle **(vehicle_reference)**.
## Feature Description:
### Identifiers and Linking Fields:
  - Unique identifier of the traffic collision: **collision_index**.
  - Official reference number of the collision: **collision_ref_no**.
  - Year in which the collision occurred: **collision_year**.
  - Identifier of the vehicle associated with the casualty: **vehicle_reference**.
  - Unique identifier of the casualty within the collision: **casualty_reference**.
### Casualty Demographics:
- Sex of the casualty (coded): **sex_of_casualty**.
- Age of the casualty in years: **age_of_casualty**.
- Categorical age group: **age_band_of_casualty**.
- Index of Multiple Deprivation (IMD) decile associated: **casualty_imd_decile**.
- Lower Super Output Area (LSOA) of the casualty (may be unknown): **lsoa_of_casualty**.
### Casualty Role and Type:
- Role of the casualty (driver, passenger, pedestrian): **casualty_class**.
- Type of casualty (coded): **casualty_type**.
- Indicator whether the casualty was a car passenger: **car_passenger**.
- Indicator whether the casualty was a bus or coach passenger: **bus_or_coach_passenger**.
- Indicator whether the pedestrian was a road maintenance worker: **pedestrian_road_maintenance_worker**.
- Location of the pedestrian at the time of the collision (if applicable): **pedestrian_location**.
- Movement of the pedestrian at the time of the collision (if applicable): **pedestrian_movement**.
### Injury Severity Information:
- Official injury severity classification (Slight / Serious/ Fatal): **casualty_severity**.
- Enhanced or derived severity classification: ** enhanced_casualty_severity**.
- Injury-based severity indicator: **casualty_injury_based**.
- Binary indicator for serious injury: **casualty_adjusted_severity_serious**.
- Binary indicator for slight injury: **casualty_adjusted_severity_slight**.
### Additional Attributes:
- Distance-based categorization related to the collision: **casualty_distance_banding**.
### Target Variable Recommendation:
- Primary Target Feature: **casualty_severity**.
- Justification:
  - Represents the final outcome of the collision on the casualty>
  - Officially defined and consistently recorded in STATS19.
  - Suitable for classifiction tasks, including:
    - Multiclass classification (Slight / Serious / Fatal).
    - Binary classification (e,g., Severe vs Non-Severe).
### Alternative Target Variables:
- **casualty_adjusted_severity_serious**.
- **casualty_injury_based**.
- **casualty_severity**.
### Typical Use Cases:
- Predicting injury severity of traffic accident casualties.
- Identifying high-risk demographic groups.
- Supporting road safety policy and intervention planning.
- Risk assessment and accident severity modeling.
### Notes and Limitations:
- All categorical variables are coded; a STATS19 data dictionary is required for interpretation.
- Some geographic and social fields may contain missing or unknown values.
