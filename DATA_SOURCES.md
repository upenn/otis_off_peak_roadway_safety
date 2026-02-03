# Data Sources & Wrangling Plan

This document tracks the progress, ownership, and details of each dataset used in the project.

## 1. Crash Data
- **Assigned to:** Kavana Raju
- **Source:** OpenDataPhilly / Client Box Folder
- **Notes:** >16K crashes, contains KSI indicators. Need to filter for relevant years (~5 years).

## 2. Speed Data
- **Assigned to:** Chi-Hyun Kim
- **Source:** Philadelphia_County_Speed_[year].csv (Client Provided)
- **Notes:** Hourly counts of vehicles by speed on 121 roads. Key dependent variable for modeling.

## 3. Volume Data
- **Assigned to:** Chi-Hyun Kim
- **Source:** PennDOT TIRE / Client Box Folder
- **Notes:** Raw axle count data. Needs to be joined with speed data to normalize rates.

## 4. Centerlines / Complete Streets Data
- **Assigned to:** Demi Yang
- **Source:** OpenDataPhilly
- **Notes:** Official road footprints. Contains basic network geometry.

## 5. RMS (Segments) Data
- **Assigned to:** Demi Yang
- **Source:** GISDATA_RMSADMIN.shp (Client Box Folder)
- **Notes:** Administrative road segments. Likely used for the primary spatial join key.

## 6. Traffic Calming Devices
- **Assigned to:** Christine Cui
- **Source:** PennDOT Open Data / Client Box Folder
- **Notes:** Speed humps, cushions, etc. Important predictor for road diet analysis.

## 7. Intersection Controls
- **Assigned to:** Christine Cui
- **Source:** OpenDataPhilly / OSM
- **Notes:** Stop signs, traffic signals. Critical for defining "intersections" vs "segments".

## 8. Streetlights
- **Assigned to:** Christine Cui
- **Source:** OpenDataPhilly
- **Notes:** Important for "Nighttime/Off-Peak" safety analysis (visibility factor).

## 9. Bike Network
- **Assigned to:** Demi Yang
- **Source:** OpenDataPhilly
- **Notes:** Bike lanes and trails. Part of the "Road Diet" characteristics.

## 10. Bus Stops / Transit Stations
- **Assigned to:** Christine Cui
- **Source:** SEPTA / OpenDataPhilly
- **Notes:** High pedestrian activity zones. May correlate with lower speeds or higher caution.

## 11. Red Light Cameras
- **Assigned to:** Christine Cui
- **Source:** OpenDataPhilly / PPA
- **Notes:** Enforcement locations. Expected to have strong correlation with driver behavior.

## 12. PA TIP (Transportation Improvement Program)
- **Assigned to:** Chi-Hyun Kim
- **Source:** DVRPC / PennDOT
- **Notes:** Planned or recent construction projects. Helps identify modified road segments.

## 13. OSM Data (OpenStreetMap)
- **Assigned to:** Chi-Hyun Kim
- **Source:** `osmdata` R package
- **Notes:** Supplemental road characteristics (lanes, speed limits, surface type) where official data is missing.
