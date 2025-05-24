# Data Dictionary: Green Taxi Data, Yellow Taxi Data, Rainfall Data

## Green Taxi Data

| Field Name            | Description                                                                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VendorID**          | A code indicating the LPEP provider that provided the record.                                                                                       |
|                       | 1 = Creative Mobile Technologies, LLC; 2 = VeriFone Inc.                                                                                            |
| **lpep_pickup_datetime**  | The date and time when the meter was engaged.                                                                                                        |
| **lpep_dropoff_datetime** | The date and time when the meter was disengaged.                                                                                                    |
| **Passenger_count**   | The number of passengers in the vehicle. This is a driver-entered value.                                                                             |
| **Trip_distance**     | The elapsed trip distance in miles reported by the taximeter.                                                                                       |
| **PULocationID**      | TLC Taxi Zone in which the taximeter was engaged.                                                                                                   |
| **DOLocationID**      | TLC Taxi Zone in which the taximeter was disengaged.                                                                                                |
| **RateCodeID**        | The final rate code in effect at the end of the trip.                                                                                               |
|                       | 1 = Standard rate                                                                                                                                    |
|                       | 2 = JFK                                                                                                                                              |
|                       | 3 = Newark                                                                                                                                           |
|                       | 4 = Nassau or Westchester                                                                                                                            |
|                       | 5 = Negotiated fare                                                                                                                                  |
|                       | 6 = Group ride                                                                                                                                       |
| **Store_and_fwd_flag**| This flag indicates whether the trip record was held in vehicle memory before sending to the vendor, aka “store and forward.”                         |
|                       | Y = store and forward trip                                                                                                                           |
|                       | N = not a store and forward trip                                                                                                                     |
| **Payment_type**      | A numeric code signifying how the passenger paid for the trip.                                                                                      |
|                       | 1 = Credit card                                                                                                                                      |
|                       | 2 = Cash                                                                                                                                             |
|                       | 3 = No charge                                                                                                                                        |
|                       | 4 = Dispute                                                                                                                                          |
|                       | 5 = Unknown                                                                                                                                          |
|                       | 6 = Voided trip                                                                                                                                      |
| **Fare_amount**       | The time-and-distance fare calculated by the meter.                                                                                                 |
| **Extra**             | Miscellaneous extras and surcharges. Currently, this only includes the \$0.50 and \$1 rush hour and overnight charges.                                 |
| **MTA_tax**           | \$0.50 MTA tax that is automatically triggered based on the metered rate in use.                                                                     |
| **Improvement_surcharge** | \$0.30 improvement surcharge assessed on hailed trips at the flag drop. The improvement surcharge began being levied in 2015.                     |
| **Tip_amount**        | Tip amount – This field is automatically populated for credit card tips. Cash tips are not included.                                                |
| **Tolls_amount**      | Total amount of all tolls paid in trip.                                                                                                             |
| **Total_amount**      | The total amount charged to passengers. Does not include cash tips.                                                                                 |
| **Trip_type**         | A code indicating whether the trip was a street-hail or a dispatch that is automatically assigned based on the metered rate in use but can be altered by the driver. |
|                       | 1 = Street-hail                                                                                                                                      |
|                       | 2 = Dispatch                                                                                                                                         |

**LPEP** (Livery Passenger Enhancement Program) is a system used in New York City's taxi and for-hire vehicle industry to monitor and improve services provided by livery vehicles, specifically **Green Taxis** or **Boro Taxis**.

**1. Purpose**:

- Introduced to enhance the service quality of Green Taxis, which are allowed to pick up passengers in outer boroughs (Brooklyn, Queens, Bronx, Staten Island) and above 110th Street in Manhattan.

- Collects trip data for monitoring purposes, similar to the TPEP (Taxi Passenger Enhancement Program) system used for Yellow Taxis.

**2. Functions**:

- **Trip Data Collection**: Records trip information, including pickup and drop-off locations, times, fares, and other related data.

- **Payment Processing**: Supports various payment methods, including credit cards and cash.

- **Driver Monitoring**: Tracks metrics like passenger counts and service efficiency.

**3. Difference from TPEP**:

- **TPEP** is for Yellow Taxis.

- **LPEP** is for Green Taxis (Boro Taxis) which operate in areas with historically lower Yellow Taxi service coverage.

This program helps the NYC Taxi and Limousine Commission (TLC) ensure regulatory compliance, improve passenger experience, and analyze transportation trends in less-served areas.

## Yellow Taxi Data

| Field Name              | Description                                                                                                                                       |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| **VendorID**            | A code indicating the TPEP provider that provided the record.                                                                                     |
|                         | 1 = Creative Mobile Technologies, LLC; 2 = VeriFone Inc.                                                                                          |
| **tpep_pickup_datetime**| The date and time when the meter was engaged.                                                                                                     |
| **tpep_dropoff_datetime**| The date and time when the meter was disengaged.                                                                                                 |
| **Passenger_count**     | The number of passengers in the vehicle. This is a driver-entered value.                                                                          |
| **Trip_distance**       | The elapsed trip distance in miles reported by the taximeter.                                                                                     |
| **PULocationID**        | TLC Taxi Zone in which the taximeter was engaged.                                                                                                 |
| **DOLocationID**        | TLC Taxi Zone in which the taximeter was disengaged.                                                                                              |
| **RateCodeID**          | The final rate code in effect at the end of the trip.                                                                                             |
|                         | 1 = Standard rate                                                                                                                                |
|                         | 2 = JFK                                                                                                                                           |
|                         | 3 = Newark                                                                                                                                        |
|                         | 4 = Nassau or Westchester                                                                                                                         |
|                         | 5 = Negotiated fare                                                                                                                               |
|                         | 6 = Group ride                                                                                                                                   |
| **Store_and_fwd_flag**  | This flag indicates whether the trip record was held in vehicle memory before sending to the vendor, aka “store and forward.”                      |
|                         | Y = store and forward trip                                                                                                                        |
|                         | N = not a store and forward trip                                                                                                                  |
| **Payment_type**        | A numeric code signifying how the passenger paid for the trip.                                                                                    |
|                         | 1 = Credit card                                                                                                                                   |
|                         | 2 = Cash                                                                                                                                          |
|                         | 3 = No charge                                                                                                                                    |
|                         | 4 = Dispute                                                                                                                                       |
|                         | 5 = Unknown                                                                                                                                       |
|                         | 6 = Voided trip                                                                                                                                   |
| **Fare_amount**         | The time-and-distance fare calculated by the meter.                                                                                               |
| **Extra**               | Miscellaneous extras and surcharges. Currently, this only includes the \$0.50 and \$1 rush hour and overnight charges.                               |
| **MTA_tax**             | \$0.50 MTA tax that is automatically triggered based on the metered rate in use.                                                                   |
| **Improvement_surcharge** | \$0.30 improvement surcharge assessed trips at the flag drop. The improvement surcharge began being levied in 2015.                              |
| **Tip_amount**          | Tip amount – This field is automatically populated for credit card tips. Cash tips are not included.                                               |
| **Tolls_amount**        | Total amount of all tolls paid in trip.                                                                                                           |
| **Total_amount**        | The total amount charged to passengers. Does not include cash tips.                                                                               |
| **Congestion_Surcharge**| Total amount collected in trip for NYS congestion surcharge.                                                                                      |
| **Airport_fee**         | \$1.25 for pick up only at LaGuardia and John F. Kennedy Airports.                                                                                 |
## Rainfall Data

-  Consider the following meteorological quantities, which are particularly used in weather radar systems.

- **Reflectivity:** Simulated from a normal distribution, e.g., N(30,5) dBZ.

  - Reflectivity is a measure of the amount of radar signal that is returned to the radar after hitting precipitation particles (like raindrops, snowflakes, or hailstones).

  - Higher values indicate more intense precipitation.

- **Radial Velocity:** Simulated from a uniform distribution, e.g., U(-20, 20) m/s.

  - Radial velocity measures the velocity of precipitation particles moving toward or away from the radar.

  - Positive values: Particles moving away from the radar (outbound).

  - Negative values: Particles moving toward the radar (inbound).

  - Helps detect wind patterns and phenomena such as rotation in storms (used to identify tornadoes).

- **Spectrum Width:** Simulated from a normal distribution, e.g., N(5, 1) m/s.

  - Spectrum width quantifies the variability or spread in radial velocity within a radar sampling volume.

  - Low values: Uniform motion (e.g., steady rain or snow).

  - High values: Turbulence or variable motion (e.g., strong winds or severe storms).

  - Indicates turbulence or changes in wind speed/direction within a storm.

- **Precipitation Simulation:**

  - Use a linear combination of the three meteorological quantities to compute hourly precipitation:

    <img width="667" alt="Screenshot 2025-04-13 at 01 11 38" src="https://github.com/user-attachments/assets/a9ef662b-30f1-45b0-accc-f01e5a1d70dc" />

  - Coefficients <img width="69" alt="Screenshot 2025-04-13 at 01 12 27" src="https://github.com/user-attachments/assets/ef668684-7884-4fee-96fc-2161c4193464" /> can be set to realistic weights (e.g., 0.6, 0.3, 0.1).

  - <img width="9" alt="Screenshot 2025-04-13 at 01 16 30" src="https://github.com/user-attachments/assets/15d6d306-f3ca-4be6-be88-80c1a3388de8" /> is random noise from <img width="100" alt="Screenshot 2025-04-13 at 01 16 40" src="https://github.com/user-attachments/assets/fc469dd3-f88c-4d5d-a9db-e52ba0108107" />.
