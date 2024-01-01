### Purpose of this work:

(Also what I learned from this work)

- Learning how can I handle 3D data & specificially LIDAR data.
- Experienced on working UAV data and/or working on geospatial projects.
- Getting a grasp for basic Compuer Vision projects (Experience on OpenCV etc.)
- This projects means new areas for me ⇒ Computer Vision and Geographical knowledge. I have no experience on this both areas, also I was newbie on DL subjects. But also I have no clue about PDAL library which you need to know to create a pipeline for your data.
- Also I start writing better code, learned new libraries which you can see my codes in /code/helpers outside from Jupyter Notebooks.

**What you will be seeing end of this explanation**: You have a lidar data that represents a place in real life that contains trees & other objects. In the end, you’ll have the trees or tree bodies which you can extract too many information from that.

I sampled 2 LIDAR data which has different part of the same city: Wellington. This city is located in New Zealand and also capital of New Zealand. Meaning that there is a city contains bunch of places that I easily collect and use. And this is the reason I chose this source. 

The 2 data source I picked from that data source contains:

- Just seperated trees
- Just trees but 2M+ points

<aside>
ℹ️ All Inputs are coming from the same source & the data source: https://doi.org/10.5069/G94Q7S68

</aside>

# *R&D Results*

**1** - **Just Seperated Trees**

*Results:*

All contours:

![AllContours](https://github.com/metin-yat/Geospatial-Lidar-Project/blob/master/final-results/just%20seperated%20trees/all_contours.png)

Just contours:

![JustContours](https://github.com/metin-yat/Geospatial-Lidar-Project/blob/master/final-results/just%20seperated%20trees/just_contours.png)

Just Convex Hulls:

![JustHulls](https://github.com/metin-yat/Geospatial-Lidar-Project/blob/master/final-results/just%20seperated%20trees/just_hulls.png)

Contours and Convex Hulls together:

![Contours&Hulls](https://github.com/metin-yat/Geospatial-Lidar-Project/blob/master/final-results/just%20seperated%20trees/hulls_%26_contours.png)



**2** -  **Large area with buildings**

*Results:*

All contours:

![AllContours](https://github.com/metin-yat/Geospatial-Lidar-Project/blob/master/final-results/large%20area/all_contours.png)

Just contours:

![JustContours](https://github.com/metin-yat/Geospatial-Lidar-Project/blob/master/final-results/large%20area/just_contours.png)

Just Convex Hulls:

![JustHulls](https://github.com/metin-yat/Geospatial-Lidar-Project/blob/master/final-results/large%20area/just_hulls.png)

Contours and Convex Hulls together:

![Contours&Hulls](https://github.com/metin-yat/Geospatial-Lidar-Project/blob/master/final-results/large%20area/hulls_%26_contours.png)


### *Conclusion*

This work detects tree bodies from a lidar taken from small to large areas. It shows poor performance when it comes to dense trees. This works definitely can show more progress than it is right now by doing:

- Correcting/changing/fixing/optimizing methods that has been used in pipelines. There is no miss usage of methods but I can see that some methods may can be replaced by other methods (smrf 2 csf etc.).
- How I generate CHM. See, there is 2 method in the internet that generates a canopy model from a dsm & dtm. One failed which I used the method that can extracts CHM properly. There may be better way to generate last model but this is not much improvements since I do not assume there too many better options for this step (With just using python & no software help like ArcGIS etc.)
- Better usage of blurring/smoothing. Since I am a beginner to all of this methods, I may use get better results by re-ordering the smoothing/blurring steps. Also expanding my knowledge on these kinda tasks may lead me not to go into complex ordered blurring steps.
Note to I optimize every smoothing/blurring line for these 2 different work. There should be better way to extract the edges from these.

Further improvements may can be do:

- Usage pre-trained models to extract these contours. Because this is not a detailed works to extract every tree and it does not use directly the Numpy file which I extracted as CHM. I use PNG of it which probably cause of losing some important information. This improvement means too much work because there is not much data that can you collect and also focuses on tree but this is not impossible.
