# Wildfire Burn Area Analysis with Google Earth Engine

This project was developed as part of the research on wildfire impact assessment using Google Earth Engine (GEE). The project includes three scripts that analyze burned areas using multispectral satellite imagery, train machine learning models, and apply pre-trained models to new fires.

## [Analyze_fire_duration](https://code.earthengine.google.com/955028071f16b7a98b7b77d205e314b5)
This script is designed to analyze the change in the differenced Normalized Burn Ratio (dNBR) over various time intervals following the start of a wildfire. The goal is to determine the optimal post-fire image acquisition window for accurate burn severity analysis. By analyzing how dNBR changes over time, the script helps in selecting the best time frame to perform the detailed analysis.

## [main](https://code.earthengine.google.com/b0f7c08462f296da2155cbecd5f6d286)
This script performs a comprehensive analysis of wildfire impact, including the training of Random Forest (RF) and Support Vector Machine (SVM) models. The analysis includes:
- Computing the dNBR and dNBR+ indices to identify burned areas.
- Training RF and SVM classifiers based on the post-fire imagery.
- Evaluating the performance of the classifiers using validation data.

By adjusting the parameters in the initial block of the script, different wildfires can be analyzed by appropriately selecting the geometry and the date of the fire event.

## [main_import](https://code.earthengine.google.com/edccde78c1e71a84e234f17c1b7d3c99)
This script also performs a full analysis of wildfire impact but instead of training new machine learning models, it imports a pre-trained RF model. The script:
- Computes the dNBR and dNBR+ indices for burn area detection.
- Applies the pre-trained RF model to classify burned areas.
- Compares the classification results with the dNBR-based estimates.

As with the `main` script, changing the parameters in the first few lines allows the analysis of different fires by selecting the appropriate geometry and date.

