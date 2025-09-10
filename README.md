# Uber & Lyft Analysis - Project Overview

## The goal of this project is to investigate the performance of Uber and Lyft rides in Boston in order to surface recommendations on pricing, demand management, and service allocation strategies

## Dataset Overview
The dataset contains ride-level information for Uber and Lyft in Boston, covering November–December 2018. It includes both raw ride attributes and engineered features that were created to support analysis on pricing, demand, and surge effects.

| Column                        | Description                                                                |
| ----------------------------- | -------------------------------------------------------------------------- |
| **id**                        | Unique identifier for each ride record.                                    |
| **cab\_type**                 | Provider of the ride (Uber or Lyft).                                       |
| **name**                      | Specific ride service/tier (e.g., UberX, Lyft XL, Black).                  |
| **price**                     | Total fare charged for the ride (USD).                                     |
| **distance**                  | Trip distance in miles.                                                    |
| **surge\_multiplier**         | Surge pricing factor applied to the ride (1 = no surge).                   |
| **hour**                      | Hour of the day when the ride was requested (0–23).                        |
| **fare\_per\_mile**           | Derived feature showing fare divided by distance.                          |
| **revenue**                   | Actual revenue from the ride (same as price).                              |
| **revenue\_expected\_normal** | Estimated revenue if no surge pricing were applied.                        |
| **revenue\_surge\_extra**     | Additional revenue earned due to surge pricing.                            |
| **spi**                       | Surge Pricing Impact (%), measuring how much surge contributes to revenue. |

## Insights Summary
In order to evaluate the rides performance, we focused on the following key metrics:
| Metric                         | Description                                                                                                                               |
| ------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Average Fare per Mile**      | The average amount riders pay per mile traveled, reflecting efficiency in pricing strategy and revenue generation.                        |
| **Surge Pricing Impact (SPI)** | Measures the effect of surge pricing on fares and revenue, indicating how much additional revenue is generated due to surge.              |
| **Price Fairness Index (PFI)** | A relative index that evaluates price competitiveness between Uber and Lyft services, helping assess whether fares are perceived as fair. |

**Average Fare per Mile**
- Across ride categories, Uber Black SUV had the highest average fare per mile ($19.43), followed by Lyft Lux Black XL ($18.77) and Lyft Lux Black ($12.76).
- While Uber and Lyft had nearly identical overall averages ($9.69 vs $9.68), Lyft consistently offered cheaper options in the economy segment, with Lyft Shared at just $3.30 per mile compared to UberPool at $5.34.
- Within premium rides, Uber Black SUV outperformed other luxury categories with a $19.43 fare per mile, whereas standard categories like UberX and Lyft averaged below $6 per mile.

**Surge Pricing Impact**
- Across ride categories, Lyft XL and Lyft had the highest average SPI (2.42%), followed closely by Lux, Lux Black XL, and Lux Black at 2.40%.
- While Lyft categories consistently showed positive SPI values, all Uber categories recorded 0.00%, pulling the overall average SPI down to just 0.97%.
- Within Lyft, Shared rides underperformed at 0.00%, standing in contrast to other Lyft categories that achieved above 2%.

**Price Fairness Index**
- Across ride categories, Lyft Shared had the lowest PFI ($1.66), making it the most efficient and rider-friendly option. Other Lyft economy rides such as Lyft ($2.65) and Lyft XL ($3.45) also maintained relatively low indexes.
- While the overall average stood at $13.71, Uber Black SUV recorded the highest PFI ($32.70), followed by Uber Black ($18.17) and Uber overall ($17.58), reflecting less efficient pricing for riders but stronger revenue capture.
- Within premium segments, Lyft Lux Black XL ($10.77) and Lyft Lux Black ($6.17) offered significantly lower PFIs than their Uber counterparts, highlighting Lyft’s stronger positioning in price fairness at the higher end.

## Recommendations
- Prioritize UberX and Lyft rides as the core service tier, since they offer the lowest fares among mainstream options ($5–6 per mile) while maintaining reasonable price fairness, making them the most competitive for volume growth.
- Promote Shared and Pool rides as the most value-for-money options (Lyft Shared $3.30/mile, PFI $1.66; UberPool $5.34/mile, PFI $7.27), positioning them as affordable and eco-friendly choices for price-sensitive users.
- Reposition premium rides (Uber Black, Lyft Lux Black) by adding differentiators such as guaranteed high-rated drivers, amenities, or business-class branding to justify higher fares, instead of competing purely on price.

## Dashboard
