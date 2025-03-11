# EDA_Optimising_NYC_Taxis_rishabhuniyal.zip
google collab link https://colab.research.google.com/drive/183R2gg6TVgW3oSWyWETtkOZMX22ilOeO?usp=sharing

For General EDA: Answer in PDF
to insert  NYC Taxi Zones in Google Colab-
    !wget -O taxi_zones.zip "https://d37ci6vzurychx.cloudfront.net/misc/taxi_zones.zip"
  extracting it= 
    import zipfile
    
    # Extract the ZIP file
    with zipfile.ZipFile("taxi_zones.zip", "r") as zip_ref:
        zip_ref.extractall("taxi_zones")
    
    print(" Shapefile extracted successfully!")
  
  and Load and Visualize the Taxi Zones
    !pip install geopandas matplotlib  # Install required libraries (if not installed)
    import geopandas as gpd
    import matplotlib.pyplot as plt
    
    # Load the shapefile
    zones = gpd.read_file("taxi_zones/taxi_zones.shp")
    
    # Plot the NYC Taxi Zones
    fig, ax = plt.subplots(figsize=(10, 10))
    zones.plot(ax=ax, edgecolor="black", alpha=0.5, cmap="coolwarm")
    plt.title("NYC Taxi Zones")
    plt.show()
    

