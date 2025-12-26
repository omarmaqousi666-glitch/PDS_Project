# UK Traffic Accidents - Casualties Dataset (STATS19)
## Overview:
This dataset contains casualty-level records from reported road traffic accidents in the United Kingdom, collected through the official STATS19 system.
Each row represents one individual casualty (injured or killed) involved in a reported traffic collision.
The dataset focuses exclusively on casualties, describing:
- Demographic characteristics of the casualty.
- The role of the casualty in the collision.
- Injury severity and adjusted severity indicators.
- Selected social and spatial attributes.
### Unit of Observation:
- One row  = one casualty (person).
- Multiple casualties may be associated with:
  - The same collision **(collision_index)**.
  - The same vehicle **(vehicle_reference)**.
### Feature Description:
- Identifiers and Linking Fields:
  - Unique identifier of the traffic collision: **collision_index**.
  - Official reference number of the collision: **collision_ref_no**.
  - Year in which the collision occurred: **collision_year**.
  - Identifier of the vehicle associated with the casualty: **vehicle_reference**.
  - Unique identifier of the casualty within the collision: **casualty_reference**.
