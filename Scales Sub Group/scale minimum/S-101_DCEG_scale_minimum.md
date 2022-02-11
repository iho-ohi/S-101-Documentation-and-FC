# 2.5.9   Sample scale minimum policy

The following policy for the application of **scale minimum** (see clause 27.149) to an ENC portfolio is based on the mandatory **maximum display scale** values listed in clause 3.4.1. While the procedure described below to determine the **scale minimum** value for features in an ENC cell is recommended, the **scale minimum** values used are at the discretion of the Producing Authority. Authorities should cooperate at the regional or RENC level to determine a **scale minimum** policy that results in suitable and consistent display of ENC data for the mariner across and, where required between, regions.

**scale minimum** values used must be selected from the following list:

| 19999999 |
| -------- |
| 9999999  |
| 4999999  |
| 3499999  |
| 1499999  |
| 999999   |
| 699999   |
| 499999   |
| 349999   |
| 259999   |
| 179999   |
| 119999   |
| 89999    |
| 59999    |
| 44999    |
| 29999    |
| 21999    |
| 17999    |
| 11999    |
| 7999     |
| 3999     |
| 2999     |
| 1999     |
| 999      |

**Table 2.6 - scale minimum values**

- **scale minimum** values for features within an ENC should be set to either 1, 2, 3 or 4 steps smaller scale than the maximum display scale of the ENC data.

- Table 2.7 below lists the step values (that is 1, 2, 3 or 4) that may be applied for specific feature classes together with any relevant conditions and additional flexibilities.

Following this process provides an automated approach to setting **scale minimum** which takes account of the relative importance of different feature classes, and will achieve sufficient de-cluttering even where there are large gaps in the scales of coverage available.

Unless the step values outlined in Table 2.7 have been manually adjusted, this approach takes no direct account of the relative importance of individual occurrences of a feature, and may result in the situation where a feature disappears and then reappears as the user zooms out on their ECDIS display. To address these remaining issues, the following additional process steps should be applied:

- Linear and area features (excluding those features subject to extensive generalisation for example **Depth Contour**) that extend beyond the coverage of a dataset and exist in an overlapping smaller scale dataset should be assigned the same **scale minimum** value as the **scale minimum** value of the corresponding feature in the smaller scale dataset.

- The **scale minimum** value of an individual occurrence of a feature should be set to either 1, 2, 3 or 4 steps smaller scale than the maximum display scale of the smallest scale ENC that the feature would appear on (that is, assuming full coverage across all compilation scales).

The following notes apply to Table 2.7 below:

1. Producers should be prepared to deviate from the step values specified when the significance of the feature dictates, for example the recommended number of steps for a **Light** feature is 4, but there will be circumstances where a **Light** feature is so important that no **scale minimum** value be applied; alternatively, the light could be so minor that a step value of 1 can be applied.

2.  **Scale minimum** should only be applied to navigational aids where they contribute to “screen clutter” and where their removal from the display does not constitute a risk to safe navigation.

3.  It is generally accepted that features making up a navigational aid will have the same attributes, and therefore features within a **Structure/Equipment** association (see clause 25.15) should be assigned the same **scale minimum** value.

4.  The elements comprising a range system (see clause 15.1.1) should have the same **scale minimum** value, which should be the value corresponding to the largest step value of the features comprising the range system. For instance, for a range system comprising a **Navigation Line**, **Recommended Track** and navigation aids, the decision may be not to apply **scale minimum** to the navigation aids (in accordance to Note 2 above), in which case the **Navigation Line** and **Recommended Track** should also not have **scale minimum** applied. Similarly, all features comprising a routeing measure (see clause 10.2) should have the same **scale minimum** value.

5.  Where features having curve or surface geometry extend over multiple **Data Coverage** areas (see clause 3.4), the value for **scale minimum** should be populated based on the value corresponding to the smallest scale value indicated by the attribute **maximum display scale** for the **Data Coverage** areas. The same approach should also be considered for items included in feature associations such as range systems and routeing measures, also taking into account Note 4 above.

## **GEO FEATURES**

| **FEATURE**                               | **PRIMITIVE**       | **CONDITION**                                                | **scale  minimum STEPS**        |
| ----------------------------------------- | ------------------- | ------------------------------------------------------------ | ------------------------------- |
| **Administration Area**                   | Surface             |                                                              | 3                               |
| **Airport/Airfield**                      | Point/Surface       | If **visual prominence** = *1* (visually conspicuous)        | 3                               |
| **Airport/Airfield**                      | Point/Surface       |                                                              | 1                               |
| **Anchor Berth**                          | Point/Surface       | If **restriction** defined                                   | 3                               |
| **Anchor Berth**                          | Point/Surface       |                                                              | 1                               |
| **Anchorage Area**                        | Point/Surface       |                                                              | 2                               |
| **Archipelagic Sea Lane Area**            | Surface             |                                                              | 4                               |
| **Archipelagic Sea Lane Axis**            | Curve               |                                                              | 4                               |
| **Beacon Cardinal**                       | Point               |                                                              | 3 (see  Notes 2,  3 &  4 above) |
| **Beacon Isolated Danger**                | Point               |                                                              | 4 (see  Notes 2,  3 &  4 above) |
| **Beacon Lateral**                        | Point               |                                                              | 3 (see  Notes 2,  3 &  4 above) |
| **Beacon Safe Water**                     | Point               |                                                              | 3 (see  Notes 2,  3 &  4 above) |
| **Beacon  Special Purpose/General**       | Point               |                                                              | 3 (see  Notes 2,  3 &  4 above) |
| **Berth**                                 | Point/Curve/Surface |                                                              | 1                               |
| **Bridge**                                | Curve/Surface       | Covered by an surface **Depth Area**, **Dredged Area**, or  **Unsurveyed Area** feature | 4                               |
| **Bridge**                                | Curve/Surface       | If  **visual prominence** = *1* (visually conspicuous) or **radar  conspicuous** = *True* and covered  by a surface **Land Area**, **Dock Area**,  or **Lock Basin** feature | 3                               |
| **Bridge**                                | Curve/Surface       |                                                              | 1                               |
| **Building**                              | Point/Surface       | If  **visual prominence** = *1* (visually conspicuous) or **radar  conspicuous** = *True* or **function** contains value *33*  (light support) | 3                               |
| **Building**                              | Point/Surface       |                                                              | 1                               |
| **Built-up Area**                         | Point/Surface       | If **visual prominence** = *1* (visually conspicuous) or  **radar conspicuous** = *True* | 3                               |
| **Built-up Area**                         | Point/Surface       |                                                              | 1                               |
| **Buoy Cardinal**                         | Point               |                                                              | 3 (see  Notes 2,  3 &  4 above) |
| **Buoy Installation**                     | Point               |                                                              | 3 (see  Notes 2,  3 &  4 above) |
| **Buoy Isolated Danger**                  | Point               |                                                              | 4 (see  Notes 2,  3 &  4 above) |
| **Buoy Lateral**                          | Point               |                                                              | 3 (see  Notes 2,  3 &  4 above) |
| **Buoy New Danger Marking**               | Point               |                                                              | 3 (see  Notes 2,  3 &  4 above) |
| **Buoy Safe Water**                       | Point               |                                                              | 3 (see  Notes 2,  3 &  4 above) |
| **Buoy Special Purpose/General**          | Point               |                                                              | 3 (see  Notes 2,  3 &  4 above) |
| **Cable Area**                            | Surface             | If **restriction** defined                                   | 3                               |
| **Cable Area**                            | Surface             |                                                              | 2                               |
| **Cable Overhead**                        | Curve               | Covered by an area  **Depth Area**, **Dredged  Area**, or  **Unsurveyed Area** feature | 4                               |
| **Cable Overhead**                        | Curve               | If **visual prominence** = *1* (visually conspicuous) or  **radar conspicuous** =  *True* | 3                               |
| **Cable Overhead**                        | Curve               |                                                              | 1                               |
| **Cable Submarine**                       | Curve               |                                                              | 3                               |
| **Canal**                                 | Curve               |                                                              | 1                               |
| **Canal**                                 | Surface             |                                                              | 4                               |
| **Cargo Transhipment Area**               | Point/Surface       |                                                              | 1                               |
| **Causeway**                              | Curve/Surface       |                                                              | 2                               |
| **Caution Area**                          | Point/Surface       |                                                              | 4                               |
| **Checkpoint**                            | Point/Surface       |                                                              | 1                               |
| **Coast Guard Station**                   | Point/Surface       |                                                              | 1                               |
| **Coastline**                             | Curve               |                                                              | NOT SET                         |
| **Collision Regulations Limit**           | Curve               |                                                              | 4                               |
| **Contiguous Zone**                       | Surface             |                                                              | 3                               |
| **Continental Shelf Area**                | Surface             |                                                              | 3                               |
| **Conveyor**                              | Curve/Surface       | Covered by an surface **Depth Area**, **Dredged Area**, or  **Unsurveyed Area** feature | 4                               |
| **Conveyor**                              | Curve/Surface       | If **visual prominence** = *1* (visually conspicuous) or  **radar conspicuous** = *True* | 3                               |
| **Conveyor**                              | Curve/Surface       |                                                              | 1                               |
| **Crane**                                 | Point/Surface       | If **visual prominence** = *1* (visually conspicuous) or  **radar conspicuous** = *True* | 3                               |
| **Crane**                                 | Point/Curve/Surface |                                                              | 1                               |
| **Current – Non-Gravitational**           | Point               |                                                              | 3                               |
| **Custom Zone**                           | Surface             |                                                              | 2                               |
| **Dam**                                   | Curve/Surface       | If seaward  edge is coincident with the coastline (see clause 8.11) | NOT SET                         |
| **Dam**                                   | Curve/Surface       | If **visual prominence** = *1* (visually conspicuous) or  **radar conspicuous** =  *True* | 3                               |
| **Dam**                                   | Curve/Surface       |                                                              | 1                               |
| **Daymark**                               | Point               | If Equipment **scale minimum** should match that of Structure | 3                               |
| **Deep Water Route  Centreline**          | Curve               |                                                              | NOT SET                         |
| **Deep Water Route Part**                 | Surface             |                                                              | NOT SET                         |
| **Depth Contour**                         | Curve               | If  **value  of depth contour** =  *0* (drying line)  or *30* | 4                               |
| **Depth Contour**                         | Curve               |                                                              | 2                               |
| **Depth – No Bottom Found**               | Pointset            |                                                              | 1                               |
| **Discoloured Water**                     | Point/Surface       |                                                              | NOT SET                         |
| **Distance Mark**                         | Point               |                                                              | 2                               |
| **Dry  Dock**                             | Surface             |                                                              | 1                               |
| **Dumping Ground**                        | Point/Surface       | If **restriction** defined                                   | 3                               |
| **Dumping Ground**                        | Point/Surface       |                                                              | 2                               |
| **Dyke**                                  | Curve/Surface       | If seaward  edge is coincident with the coastline (see clause 8.5) | NOT SET                         |
| **Dyke**                                  | Curve/Surface       |                                                              | 1                               |
| **Exclusive Economic Zone**               | Surface             |                                                              | 3                               |
| **Fairway**                               | Surface             |                                                              | 3                               |
| **Fence/Wall**                            | Curve               | If **visual prominence** = *1* (visually conspicuous) or  **radar conspicuous** = *True* | 3                               |
| **Fence/Wall**                            | Curve               |                                                              | 1                               |
| **Ferry Route**                           | Curve/Surface       |                                                              | 3                               |
| **Fishery Zone**                          | Surface             |                                                              | 3                               |
| **Fishing Facility**                      | Point/Curve/Surface |                                                              | 2                               |
| **Fishing Ground**                        | Surface             |                                                              | 1                               |
| **Floating Dock**                         | Point/Curve         | If **visual prominence** = *1* (visually conspicuous) or  **radar conspicuous** = *True* | 3                               |
| **Floating Dock**                         | Point/Curve         |                                                              | 1                               |
| **Floating Dock**                         | Surface             |                                                              | NOT SET                         |
| **Fog  Signal**                           | Point               | If  Equipment **scale minimum** should  match that of Structure | 3                               |
| **Fortified Structure**                   | Point/Curve/Surface | If **visual prominence** = *1* (visually conspicuous) or  **radar conspicuous** = *True* | 3                               |
| **Fortified Structure**                   | Point/Curve/Surface |                                                              | 1                               |
| **Foul Ground**                           | Point/Curve/Surface | If  **value of sounding** > *30* and **exposition of sounding** ? *2* (shoaler than range of the surrounding depth area) | 4                               |
| **Foul Ground**                           | Point/Curve/Surface |                                                              | NOT SET                         |
| **Free Port Area**                        | Surface             |                                                              | 2                               |
| **Gate**                                  | Point/Curve/Surface | Covered by an surface **Depth Area**, **Dredged Area**, or  **Unsurveyed Area** feature | NOT SET                         |
| **Gate**                                  | Point/Curve/Surface |                                                              | 2                               |
| **Gridiron**                              | Surface             |                                                              | 1                               |
| **Harbour Area (Administrative)**         | Surface             |                                                              | 3                               |
| **Harbour Facility**                      | Point/Surface       |                                                              | 1                               |
| **Hulk**                                  | Point               | If **visual prominence** = *1* (visually conspicuous) or  **radar conspicuous** =  *True* | 3                               |
| **Hulk**                                  | Point               |                                                              | 1                               |
| **Hulk**                                  | Surface             |                                                              | NOT SET                         |
| **Ice  Area**                             | Surface             |                                                              | 3                               |
| **Information Area**                      | Point/Curve/Surface |                                                              | 2                               |
| **Inshore Traffic Zone**                  | Surface             |                                                              | NOT SET                         |
| **Lake**                                  | Surface             |                                                              | 1                               |
| **Land Area**                             | Surface             |                                                              | NOT SET                         |
| **Land Area**                             | Point/Curve         |                                                              | 4                               |
| **Land Elevation**                        | Point               | If **visual prominence** = *1* (visually conspicuous)        | 3                               |
| **Land Elevation**                        | Point/Curve         |                                                              | 1                               |
| **Land Region**                           | Point/Curve/Surface |                                                              | 1                               |
| **Landmark**                              | Point/Curve/Surface | If  **visual prominence** = *1* (visually conspicuous) or **radar  conspicuous** = *True* or **function** contains value *33*  (light support) | 3                               |
| **Landmark**                              | Point/Curve/Surface |                                                              | 1                               |
| **Light Air Obstruction**                 | Point               | If  Equipment **scale minimum** should  match that of Structure | 4 (see  Notes 2,  3 &  4 above) |
| **Light All Around**                      | Point               | If Equipment **scale  minimum** should match that of Structure | 4 (see  Notes 2,  3 &  4 above) |
| **Light Float**                           | Point               |                                                              | 4 (see  Notes 2,  3 &  4 above) |
| **Light Fog Detector**                    | Point               | If  Equipment **scale minimum** should  match that of Structure | 4 (see  Notes 2,  3 &  4 above) |
| **Light Sectored**                        | Point               | If  Equipment **scale minimum** should  match that of Structure | 4 (see  Notes 2,  3 &  4 above) |
| **Light Vessel**                          | Point               |                                                              | 4 (see  Notes 2,  3 &  4 above) |
| **Local Magnetic Anomaly**                | Point/Curve/Surface |                                                              | 3                               |
| **Log  Pond**                             | Point/Surface       | Covered by an surface **Depth Area**, **Dredged Area**, or  **Unsurveyed Area** feature | 4                               |
| **Log  Pond**                             | Point/Surface       |                                                              | 1                               |
| **Magnetic Variation**                    | Point/Curve/Surface |                                                              | 1                               |
| **Marine Farm/Culture**                   | Point/Curve/Surface | If  **exposition of sounding** = *2* (shoaler than range of the surrounding depth area) and **value of sounding** ? *30* | 4                               |
| **Marine Farm/Culture**                   | Point/Curve/Surface | If **restriction** defined                                   | 3                               |
| **Marine Farm/Culture**                   | Point/Curve/Surface |                                                              | 1                               |
| **Marine  Pollution Regulations Area**    | Surface             |                                                              | 3                               |
| **Military Practice Area**                | Point/Surface       |                                                              | 3                               |
| **Mooring/Warping Facility**              | Point/Curve/Surface | If **visual prominence** = *1* (visually conspicuous) or  **radar conspicuous** =  *True* | 3                               |
| **Mooring/Warping Facility**              | Point/Curve/Surface |                                                              | 2                               |
| **Navigation Line**                       | Curve               |                                                              | 3                               |
| **Obstruction**                           | Point/Curve/Surface |                                                              | NOT SET                         |
| **Obstruction**                           | Point/Curve/Surface | If  **value of sounding** > *30* and **exposition of sounding** ? *2* (shoaler than range of the surrounding depth area) | 4                               |
| **Offshore Platform**                     | Point/Surface       | Covered by a surface **Offshore Production Area**            | 3                               |
| **Offshore Platform**                     | Point/Surface       |                                                              | 4                               |
| **Offshore Production Area**              | Surface             |                                                              | 4                               |
| **Oil  Barrier**                          | Curve               |                                                              | 4                               |
| **Physical AIS Aid to Navigation**        | Point               |                                                              | 3 (see  Notes 2,  3 &  4 above) |
| **Pile**                                  | Point               | Where used to mark  position of **Light** feature in water   | 4  (see Notes 3  & 4 above)     |
| **Pile**                                  | Point/Curve/Surface | If **visual prominence** = *1* (visually conspicuous)        | 3                               |
| **Pile**                                  | Point/Curve/Surface |                                                              | 2                               |
| **Pilot Boarding Place**                  | Point/Surface       |                                                              | 3                               |
| **Pilotage District**                     | Surface             |                                                              | 3                               |
| **Pipeline Overhead**                     | Curve               | Covered by a surface **Depth Area**, **Dredged Area**, or  **Unsurveyed Area** feature | 4                               |
| **Pipeline Overhead**                     | Curve               | If **visual prominence** = *1* (visually conspicuous) or  **radar conspicuous** = *True* | 3                               |
| **Pipeline Overhead**                     | Curve               |                                                              | 1                               |
| **Pipeline Submarine/On Land**            | Curve               | Covered by a surface **Depth Area**, **Dredged Area**, or  **Unsurveyed Area** feature | 3                               |
| **Pipeline Submarine/On Land**            | Curve               |                                                              | 1                               |
| **Pontoon**                               | Point/Curve         | If **visual prominence** = *1* (visually conspicuous) or  **radar conspicuous** =  *True* | 3                               |
| **Pontoon**                               | Point/Curve         |                                                              | 2                               |
| **Pontoon**                               | Surface             |                                                              | 4                               |
| **Precautionary Area**                    | Point/Surface       |                                                              | NOT SET                         |
| **Production/Storage Area**               | Point/Surface       | If **visual prominence** = *1* (visually conspicuous) or  **radar conspicuous** = *True* | 3                               |
| **Production/Storage Area**               | Point/Surface       |                                                              | 1                               |
| **Pylon/Bridge Support**                  | Point/Surface       | Covered by a surface **Depth Area**, **Dredged Area**, or  **Unsurveyed Area** feature | NOT SET                         |
| **Pylon/Bridge Support**                  | Point/Surface       | If **visual prominence** = *1* (visually conspicuous) or  **radar conspicuous** = *True* | 3                               |
| **Pylon/Bridge Support**                  | Point/Surface       |                                                              | 1                               |
| **Radar Line**                            | Curve               |                                                              | 3                               |
| **Radar Range**                           | Surface             |                                                              | 3                               |
| **Radar Reflector**                       | Point               | If  Equipment **scale minimum** should  match that of Structure | 3                               |
| **Radar Station**                         | Point               | If  Equipment **scale minimum** should  match that of Structure | 2                               |
| **Radar Transponder Beacon**              | Point               | If  Equipment **scale minimum** should  match that of Structure | 3                               |
| **Radio Calling-In Point**                | Point/Curve         |                                                              | 3                               |
| **Radio Station**                         | Point               | If  Equipment **scale minimum** should  match that of Structure | 1                               |
| **Railway**                               | Curve               |                                                              | 1                               |
| **Rapids**                                | Point/Curve/Surface |                                                              | 1                               |
| **Recommended Route Centreline**          | Curve               |                                                              | 3                               |
| **Recommended Track**                     | Curve               |                                                              | 3                               |
| **Recommended Traffic Lane Part**         | Point/Surface       |                                                              | 3                               |
| **Rescue Station**                        | Point/Surface       |                                                              | 3                               |
| **Restricted Area Navigational**          | Surface             |                                                              | 3                               |
| **Restricted Area Regulatory**            | Surface             |                                                              | 3                               |
| **Retroreflector**                        | Point               | If  Equipment **scale minimum** should  match that of Structure | 3                               |
| **River**                                 | Curve               |                                                              | 1                               |
| **River**                                 | Surface             |                                                              | 4                               |
| **Road**                                  | Curve/Surface       |                                                              | 1                               |
| **Runway**                                | Point/Curve/Surface | If **visual prominence** = *1* (visually conspicuous)        | 3                               |
| **Runway**                                | Point/Curve/Surface |                                                              | 1                               |
| **Sandwave**                              | Point/Curve/Surface |                                                              | 3                               |
| **Sea  Area/Named Water Area**            | Point/Surface       |                                                              | 1                               |
| **Seabed Area**                           | Point/Curve/Surface |                                                              | 1                               |
| **Seagrass**                              | Point/Surface       |                                                              | 3                               |
| **Seaplane Landing Area**                 | Point/Surface       | If **restriction** defined                                   | 3                               |
| **Seaplane Landing Area**                 | Point/Surface       |                                                              | 1                               |
| **Shoreline Construction**                | Point/Curve/Surface |                                                              | NOT SET                         |
| **Signal Station Traffic**                | Point/Surface       | If  Equipment **scale minimum** should  match that of Structure | 1                               |
| **Signal Station Warning**                | Point/Surface       | If  Equipment **scale minimum** should  match that of Structure | 1                               |
| **Silo/Tank**                             | Point/Surface       | If **visual prominence** = *1* (visually conspicuous) or  **radar conspicuous** = *True* | 3                               |
| **Silo/Tank**                             | Point/Surface       |                                                              | 1                               |
| **Slope Topline**                         | Curve               | If **visual prominence** = *1* (visually conspicuous) or  **radar conspicuous** = *True* | 3                               |
| **Slope Topline**                         | Curve               |                                                              | 1                               |
| **Sloping Ground**                        | Point/Surface       | If **visual prominence** = *1* (visually conspicuous) or  **radar conspicuous** = *True* | 3                               |
| **Sloping Ground**                        | Point/Surface       |                                                              | 1                               |
| **Small Craft Facility**                  | Point/Surface       |                                                              | 1                               |
| **Sounding**                              | Pointset            |                                                              | 1                               |
| **Span Fixed**                            | Curve/Surface       |                                                              | NOT SET                         |
| **Span Opening**                          | Curve/Surface       |                                                              | NOT SET                         |
| **Spring**                                | Point               |                                                              | 1                               |
| **Straight Territorial Sea Baseline**     | Curve               |                                                              | 3                               |
| **Submarine Pipeline Area**               | Point/Surface       |                                                              | 3                               |
| **Submarine Transit Lane**                | Surface             |                                                              | 3                               |
| **Swept Area**                            | Surface             |                                                              | 3                               |
| **Territorial Sea Area**                  | Surface             |                                                              | 3                               |
| **Tidal Stream – Flood/Ebb**              | Point/Surface       |                                                              | 3                               |
| **Tidal Stream Panel Data**               | Point/Surface       |                                                              | 2                               |
| **Tideway**                               | Curve/Surface       |                                                              | 1                               |
| **Traffic Separation Line**               | Curve               |                                                              | NOT SET                         |
| **Traffic  Separation Scheme Boundary**   | Curve               |                                                              | NOT SET                         |
| **Traffic  Separation Scheme Crossing**   | Surface             |                                                              | NOT SET                         |
| **Traffic  Separation Scheme Lane Part**  | Surface             |                                                              | NOT SET                         |
| **Traffic  Separation Scheme Roundabout** | Surface             |                                                              | NOT SET                         |
| **Traffic Separation Zone**               | Surface             |                                                              | NOT SET                         |
| **Tunnel**                                | Curve/Surface       | Covered by a surface **Depth Area**, **Dredged Area**, or  **Unsurveyed Area** feature | 4                               |
| **Tunnel**                                | Curve/Surface       |                                                              | 1                               |
| **Two-Way Route Part**                    | Surface             |                                                              | NOT SET                         |
| **Underwater/Awash Rock**                 | Point               | If  **value of sounding** > *30* and **exposition of sounding** ? *2* (shoaler than range of the surrounding depth area) | 4                               |
| **Underwater/Awash Rock**                 | Point               | Covered by an surface **Obstruction** feature                | 2                               |
| **Underwater/Awash Rock**                 | Point               |                                                              | NOT SET                         |
| **Vegetation**                            | Point/Curve/Surface | If **visual prominence** = *1* (visually conspicuous)        | 3                               |
| **Vegetation**                            | Point/Curve/Surface |                                                              | 1                               |
| **Vessel Traffic Service Area**           | Surface             |                                                              | 3                               |
| **Virtual AIS Aid to Navigation**         | Point               |                                                              | 3 (see  Notes 2,  & 4 above)    |
| **Water Turbulence**                      | Point/Curve/Surface |                                                              | 3                               |
| **Waterfall**                             | Point/Curve         | If **visual prominence** = *1* (visually conspicuous)        | 3                               |
| **Waterfall**                             | Point/Curve         |                                                              | 1                               |
| **Weed/Kelp**                             | Point/Surface       |                                                              | 3                               |
| **Wind Turbine**                          | Point               | On  land and if **visual prominence** = *2* (not visually conspicuous) or *3*  (prominent) | 1                               |
| **Wind Turbine**                          | Point               | Covered by a surface **Offshore Production Area**            | 3                               |
| **Wind Turbine**                          | Point               |                                                              | 4                               |
| **Wreck**                                 | Point/Surface       | If  **category of wreck** = *1* or (**value of sounding** > *30* and **exposition of sounding** ? *2* (shoaler  than range of the surrounding depth area)) | 3                               |
| **Wreck**                                 | Point/Surface       | If **visual prominence** = *1* (visually conspicuous) or  **radar conspicuous** = *True* | 3                               |
| **Wreck**                                 | Point/Surface       |                                                              | NOT SET                         |

**METADATA FEATURES**

| **Local Direction of Buoyage** | Surface             |      | 4       |
| ------------------------------ | ------------------- | ---- | ------- |
| **Update Information**         | Point/Curve/Surface |      | NOT SET |

**CARTOGRAPHIC FEATURES**

| **Text Placement** | Point |      | <= associated feature |
| ------------------ | ----- | ---- | --------------------- |
|                    |       |      |                       |

**Table 2.7 – Procedure for determining scale minimum values - Example**

Optional additional rules that can be manually applied to fine tune the application of **scale minimum**

after the above values have been automatically applied.

| **GEO  FEATURE**             | **PRIMITIVE** | **CONDITION**                                                | **scale  minimum STEPS** |
| ---------------------------- | ------------- | ------------------------------------------------------------ | ------------------------ |
| **Obstruction**              | Point         | The most  significant **Obstruction** of a group of  **Obstruction**s within  close proximity | NOT SET                  |
| **Obstruction**              | Point         | For  groups of **Obstruction**s in close  proximity, or within an **Obstruction** surface | 2                        |
| **Sounding**                 | Pointset      | **scale minimum**  should be applied so that the least significant soundings are set to 1 step progressing to 4 steps for the most significant, above the  compilation scale in order to  achieve a gradual reduction in the soundings displayed as the user  zooms out. | 1, 2, 3,  4              |
| **Depth – No Bottom  Found** | Pointset      | **scale minimum** should  be applied so that the least significant depths are set to 1 step progressing to 4 steps  for the most significant, above the compilation scale in order to achieve a gradual reduction in  the depths displayed as the user  zooms out. | 1, 2, 3,  4              |
| **Underwater/Awash Rock**    | Point         | The  most significant **Underwater/Awash Rock**  of a group of **Underwater/Awash Rock**s within close proximity and not within  an **Obstruction** surface | NOT SET                  |
| **Wreck**                    | Point/Surface | For  groups of **Wreck** in close proximity  (the most significant should  not have **scale minimum**) | 2                        |

**Table 2.8 - Additional scale minimum considerations - Examples**