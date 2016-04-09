# B Viewing Data

## B.1 Data Layer 

### To open a file in Focus:

##### In the menu select File -> Open. The File Selector dialog opens.

![](./img/mod01-b-01.png)

##### In your working folder click irvine.pix. Click Open.

![](./img/mod01-b-02.png)

![](./img/mod01-b-03.png)

In the control panel on the left of the Focus window an unnamed map with a new area and a RGB (red, green, blue) layer is automatically added.

The RGB layer displays a Landsat multispectral image of Irvine, California in the Focus view area.

### To show or hide a layer:

##### Click on the check box on the left of the RGB Irvine.pix:1,2,3 layer. Notice the check disappears - the layer is now hidden. The viewing area will be blank.

![](./img/mod01-b-04.png)

### To add a layer with the Add Layer Wizard:

##### Right click on the New Area icon in the Maps tree.

##### In the context menu select Add...

![](./img/mod01-b-05.png)

![](./img/mod01-b-06.png)

##### In the Add Layer Wizard, select Grayscale for the type of layer you want to add. Click Next.

![](./img/mod01-b-07.png)

##### In the Add Layer Wizard, click Browse.

![](./img/mod01-b-08.png)

##### In the file selector dialog, navigate to your working directory, locate and select eltoro.pix. 7. Click Open.

![](./img/mod01-b-09.png)

##### In the available channels list, click the only available channel which is SPOT HRV1 Panchromatic (0.51-0.73um). In the Add Layer Wizard, click Finish.

![](./img/mod01-b-10.png)

![](./img/mod01-b-11.png)

### The Files Tree

##### Click on the Files tab in the control pane. You can now see the Files tree, a list of available files – irvine.pix and eltoro.pix, and their components.

![](./img/mod01-b-12.png)

The components listed will depend on the data available and processing that has occurred on the data. In the above example eltoro.pix contains rasters and look up tables, where Irvine.pix contains rasters, vectors, bitmaps, lookup tables, pseudocolor tables, ground control points and signatures.

##### Data are organized into different components depending on type, there are three types of data: raster, vector and auxiliary.

 - Rasters are stored in channels. These are your images you will be working with during this course.
􏰀
 - Vectors are stored in segments. These are your geographic points, lines and polygons representing features e.g. a road.
􏰀
 - Bitmaps, Lookup Tables, Pseudocolor Tables, Ground Control Points and Signatures are also stored in segments, these are **auxiliary data** used to assist in interpretation and analysis.

### To Add a Layer to the view from the Files tree:

##### Expand the vectors component list from the irvine.pix file by clicking on the “+” beside it.

The available vector data are shown in the list. The vectors are organized in segments and all segemets are numbered. In this file segments 25 to 31 (minus 27) contain vector data.

![](./img/mod01-b-13.png)

##### Right-click on the first segment, number 25, DLGTRANS:VED transportation..., and select View from the context menu .

![](./img/mod01-b-14.png)

![](./img/mod01-b-15.png)

##### Switch back to the Maps tree in the control pane by clicking on the Maps tab.

![](./img/mod01-b-16.png)

##### You should now have three (3) layers listed under the new area of your unnamed map – 1 vector layer, 1 grayscale layer and 1 RGB layer.

### The Layer Manager

##### From the Layer menu of the Focus menu bar, select Layer Manager. (at the bottom)

![](./img/mod01-b-17.png)

![](./img/mod01-b-18.png)

### To change Layer Visibility in the Layer Manager:

##### In the Layer Visible Column, deselect the transportation and eltoro layers. Click on the green check mark – the check will disappear. Click Ok.

![](./img/mod01-b-19.png)

![](./img/mod01-b-20.png)

Changes in the Layer Manager are shown in the Maps tree automatically when you click Ok or Apply.

## B.2 Properties

### Layer Properties

##### In the Maps tree, right-click on the RGB irvine.pix:1,2,3 layer. A context menu appears. Select Properties at the bottom.

![](./img/mod01-b-21.png)

![](./img/mod01-b-22.png)

##### In the Layer Properties window:

- The **General** tab indicates the name of the layer, its priority, the resample method, and current enhancement for that layer.

- The **Source Images** tab lists which raster data sets are displayed as RGB, and which file the data are from.

- The **Source LUTs** tab displays available look up tables for each raster.

- In the **Display** tab, you can alter transparency for each dataset and opacity for the layer.

- Finally, the **Display within Zoom Scale** tab allows you to specify a zoom scale for the layer.

##### Click on the Display tab in the RGB Layer Properties window.

##### Select the Transparency option by clicking the in the white box beside it.

![](./img/mod01-b-23.png)

##### Specify the values 20:255 in each of the three available boxes (Red Values, Green Values, and Blue Values).

![](./img/mod01-b-24.png)

##### Click Apply.

##### Turn off the vector and grayscale layers.

![](./img/mod01-b-25.png)

The low pixel values 0-19 from each data set remain visible in the viewer while all other values (20-255) become transparent. This is useful for removing particular pixel value ranges in order to more easily visualize your data. This is in effect display a selection or sub-set of the data.

##### To return to normal display, deselect the transparency option. And click Apply then OK to close the RGB Layer Properties dialog.

![](./img/mod01-b-26.png)

![](./img/mod01-b-27.png)

### File Properties

##### In the Files tree (activate by clicking on the Files tab of the control pane), right-click on the Irvine.pix file.

##### Select Properties from the menu list. The File Properties panel opens. (image below/next page).

![](./img/mod01-b-28.png)

##### On the General pane notice the Raster Size: 512P by 512L. This means the Irvine file stores a raster as 512 pixels by 512 lines (columns and rows).

![](./img/mod01-b-29.png)

##### Switch to the Projection tab and notice each pixel (Pixel Size X: 30 meters) in the 512X512 image is 30 meters in size. Also notice the spatial reference for the dataset. UTM 11 S E000.

![](./img/mod01-b-30.png)

From this you can calculate the ground coverage of your data. 512 pixels multiplied by 30 meters equals a width of 15360 meters or 15.36 km.

##### Click OK to close the File Properties dialog.











