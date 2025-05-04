🛢️ Oil Spill Detection from Satellite Imagery using Sentinel-1 and Random Forest

This project uses Sentinel-1 Synthetic Aperture Radar (SAR) imagery and Google Earth Engine to detect oil spills in water bodies through supervised classification using the Random Forest algorithm. The method leverages backscatter intensity changes (dark spots) associated with oil slicks.
📍 Project Objectives

    Detect oil spills from satellite radar imagery

    Use supervised classification with Random Forest

    Generate classified oil spill maps for visualization and export

    Support oil spill monitoring and environmental management in coastal areas

🛰️ Data Source

    Satellite: Sentinel-1 GRD

    Band Used: VV polarization (Vertical transmit and receive)

    Temporal Coverage: January 2023 (can be adjusted)

    Area of Interest (AOI): Niger Delta coastal region (editable)

🧰 Tools & Technologies

    Google Earth Engine (Python API)

    Python 3.8+

    geemap, earthengine-api, folium

🚀 How to Run
1. Install Required Packages

pip install earthengine-api geemap folium

2. Authenticate and Initialize Earth Engine

earthengine authenticate

3. Run the Python Script

Execute the Python script (oil_spill_rf.py) to perform the following:

    Load and pre-process Sentinel-1 SAR imagery

    Label training data (oil spill and open water)

    Train Random Forest classifier

    Classify entire scene

    Visualize classified map and optionally export to Google Drive

📊 Sample Output Layers

    Sentinel-1 VV – SAR backscatter intensity

    Oil Spill (RF) – Pixels classified as oil spill (Red)

    Non-Spill (RF) – Pixels classified as open water (Blue)

📁 File Structure

.
├── oil_spill_rf.py            # Main detection script
├── training_data.geojson      # Optional training points (if exporting from GEE)
├── classified_output.tif      # Exported classified map
├── README.md                  # Project overview

📌 Key Notes

    Oil spills appear as dark patches due to reduced radar backscatter.

    Threshold-based methods are limited; machine learning improves accuracy.

    You can refine the model by adding more training points and bands (e.g., VH).

    Use NDPI or texture features for more robust detection.

📚 References

    Solberg, A. H. S., et al. (2007). "Automatic Detection of Oil Spills in ERS SAR Images." IEEE Transactions on Geoscience and Remote Sensing.

    Copernicus Open Access Hub: https://scihub.copernicus.eu/

    GEE Docs: https://developers.google.com/earth-engine

🔐 License

This project is open-source and available under the MIT License.
