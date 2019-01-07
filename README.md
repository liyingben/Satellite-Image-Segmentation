# Satellite_Image_Segmentation

DISCLAIMER: 
    This project is not yet fully functional. For a preview of the final output please see Final_Output.ipynb 
    The pytorch model is not fully tested yet. The data pre-processing is done and tested.

OVERVIEW OF THE PROJECT:
    The challenge of this project is to predict each pixel of the image rather than just a category label.

ABOUT THE DATA : 
    1km x 1km satellite images in both 3-band and 16-band formats. All images are in GeoTiff format
     The goal is to detect and classify the types of objects found in these regions. 
     In a satellite image, you will find lots of different objects like roads,
     buildings, vehicles, farms, trees, water ways,  etc. Dstl has labeled 10 different classes:

    Buildings - large building, residential, non-residential, fuel storage facility, fortified building
    Misc. Manmade structures 
    Road 
    Track - poor/dirt/cart track, footpath/trail
    Trees - woodland, hedgerows, groups of trees, standalone trees
    Crops - contour ploughing/cropland, grain (wheat) crops, row (potatoes, turnips) crops
    Waterway 
    Standing water
    Vehicle Large - large vehicle (e.g. lorry, truck,bus), logistics vehicle
    Vehicle Small - small vehicle (car, van), motorbike

    Every object class is described in the form of Polygons and MultiPolygons, which are simply a list of polygons. 
    There are two different formats for these shapes: GeoJson and WKT. 
    
LINK TO THE ARCHITECTURE OF UNET MODEL: https://arxiv.org/pdf/1505.04597.pdf

    
FILES IN THE PROJECT:
1. Put the download the data from https://www.kaggle.com/c/dstl-satellite-imagery-feature-detection
and put it in the data folder
2. The Final_Output file contains a preview of how the project output would look like on completion
3. Data Exploration can be used to see the various formats of data in the dataset and how to use them
4. Train_model notebook contains the code for data preprocessing (i.e converting different formats into numpy that can be used by the model), it contains the code for building a U_NET model and steps for training it.
    