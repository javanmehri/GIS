### 1 - Create a new Map

##### Make sure Focus is running and start with a new project (File -> new project).

![](./img/Ex01-01.png)

##### On the Maps toolbar, select the New Map button to establish a map and area within the viewer.

![](./img/Ex01-02.png)

![](./img/Ex01-03.png)

The Maps tree should have two entries: one for a map and one for an area within the map. Notice that each layer has a specific symbol attached to it.

### 2 - Rename

##### Rt-Click on the Unnamed Map, and select properties.

![](./img/Ex02-01.png)

##### In the Map Properties, in the Name: section of the General tab Change the name from Unnamed Map to “Irvine, California”.

![](./img/Ex02-02.png)

##### Click OK to close the dialog and apply the changes.

##### Double-click the new area layer to open the Area Properties dialog box. In the Name text field in the Generic section on the General tab enter the following text: “Color Infrared Composite”. Click OK to accept the text change, and close the dialog box.

![](./img/Ex02-03.png)

### 3 - Add Data to a map

##### On the maps toolbar, click the Add Layer button to open the Add Layer Wizard. Select the RGB option then click next>. Click Browse to locate and open irvine.pix from your working directory. Once opened, a list of all the available channels in irvine.pix will appear in the list box. Select (click once on) channels 5, 3 and 1 for the red, green and blue color guns, respectively. Click Finish.

![](./img/Ex03-01.png)

![](./img/Ex03-02.png)

##### This layer has been assigned a default name. Use the steps outlined above to rename the layer to read: “TM Bands 5,3,1”

![](./img/Ex03-03.png)

##### Click the + next to the RGB layer to display the list of data that the layer is comprised of.

![](./img/Ex03-04.png)

### 4 - Add a second Area to the map

##### On the Maps toolbar, click the New Area button in order to add a second area within the map.

##### As before, by default, it will be labeled “New Area”. Change this area’s text to read: “LULC Classification”.

##### Select this newly created area (it will be highlighted) then on the maps toolbar, select the the Add Layer Wizard button.

##### From the Add Layer Wizard select the Pseudocolor option then click next>. A list of all the available image channels in irvine.pix will appear in the list box. Select channel 6 (USGS Land Use / Land Cover). Click Finish.

You have now entered a pseudo-colored layer to the LULC Classification area in the Irvine California Map displayed in the Maps tree. The symbol for this layer is shown accompanying the layer’s tree
entry. 

A pseudo-color layer is an image with different colors (red, green, blue etc) assigned to different digital numbers within the same image layer.
Pseudo-color layers are used to display a thematic map. The image you are displaying is a land use/ land cover thematic map for the Irvine area.

##### Click on the plus next to the pseudo-color layer to view the legend. You should see a legend like the partial display below.

##### Look at the image and the legend; notice the different colors for the different land use/land cover classifications.

### 5 - Geomatica Project Files


