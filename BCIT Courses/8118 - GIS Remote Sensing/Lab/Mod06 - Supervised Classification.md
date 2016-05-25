# classification

- Start the FOCUS application. If it is not running. Make sure you have a blank empty project

- From the Analysis menu, click Image Classification and then click Supervised.

![](./img/m06-01.png)

- In the File Selector dialog box, locate and select an image file you want to classify, in this lab you will classify l7_rf_nvan.pix.

![](./img/m06-02.png)

- Click Open. The Session selection dialog opens.

![](./img/m06-03.png)

As you have not started a classification your session is blank.

- Click New Session to define the classification session. A session configuration dialog opens (image below)

![](./img/m06-04.png)

- Click on the [add Layer...] button. This will open the Add Image Channels to: dialog.

![](./img/m06-05.png)

- In the entry field next to 8 bit enter 2 (image below) to add two new channels.

![](./img/m06-06.png)

- Select [Add] . Then [Close] to close the dialog.

![](./img/m06-07.png)

Notice two new channels (7 and 8) have been added to your database, the l7_rf_nvan.pix file.

### Configure the classification session

- Enter Supervised classification ETM3 and ETM4 tutorial for the description

![](./img/m06-08.png)

- Set ETM5,ETM4,ETM2 as the Red, Green, Blue display – click in the cell to set the check mark in that location.

![](./img/m06-09.png)

- Select channel 7 as the training channel, channel 8 as the output channel, and ETM3 and ETM4 as the input channels - click in the cell. 

![](./img/m06-10.png)

- Select [OK] when done.

The Focus display will change to display a Classification MetaLayer, and a Training Site Editor dialog will open (image below).

![](./img/m06-11.png)

You will now enter some training data. The training data are known locations of a selected land cover. For this exercise you will identify grass, clear water, sediment water and conifers forest. Vectors identifying locations of each of these classes have been provided in the l7_rf_nvan.pix database.

- Add the grass field, clear water, sediment water and coniferous forest vectors to your map display. (From the files tree rt-click and select view on the vector segment.)

![](./img/m06-12.png)

![](./img/m06-13.png)

- Zoom to overview of layer on the grass field layer. Zoom out a few times until you can see the entire boundary of the grass field.

![](./img/m06-14.png)

![](./img/m06-15.png)

- Click once on the Training Areas layer and make sure the pencil is located next to the pseudocolor symbol (image below).

![](./img/m06-16.png)

The pencil indicates this is the layer that will be edited.

If your Training Site Editor dialog is not open RT-CLICK on Classification MetaLayer and select Open Training Sites to reopen the dialog.

- In the Training sites Editor dialog select Class -> new.

![](./img/m06-17.png)

A new class with id 1, value of 1 and a name of Class-01 with the color green will appear on the list

![](./img/m06-18.png)

The Value is the DN that will be entered into all pixels in channel 7 of your database that are identified as a grass training areas.

Threshold and Bias are for advanced classification and we will not work with them at this time.

- Double-Click in the Name cell to change the name from Class-01 to Grass.

- Make sure the pencil is still next to the Training areas layer. From the new shapes dropdown list (upper left of the Focus window, image below) Select Rectangle

![](./img/m06-19.png)

- In your Focus display window draw a rectangle for the grass area.

![](./img/m06-20.png)

- Now switch your tool to the select tool by clicking on the black arrow in the upper left of the FOCUS window. This is the least damaging tool when editing.

![](./img/m06-21.png)

Although you drew a vector rectangle what the software did was set the pixel/cell values under your rectangle to 1. Thus you do not have a vector but a collection of pixels with a DN of 1. The 1 is from the class value set in the Training Sites Editor dialog. 

To erase a training site click on the Raster Erase tool (to the right of the new shapes tool) and select erase polygon. Draw a polygon around the training site you want to erase. The area you traced will be ‘deleted’ i.e. the pixel values will be set back to zero. On the layer with the pencil.

![](./img/m06-22.png)

- Select the Save button from the Training Sites Editor to save your training area.

![](./img/m06-23.png)

- Now repeat the steps to enter a training site for clear water (value 2), sediment water (value 3) and conifers forest (value 4). Make sure to save frequently. 

![](./img/m06-24.png)

### Training site evaluation (how good are my sites?)

- Now that you have some classes with training sites defined you need to look at ‘how good’ are your training sites. Your training sites should not statistically overlap. You can view:

 - the class ellipse on a scatter plot of two bands,
 - check for signature separability,
 - view the signature statistics and
 - view a histogram of the DN of the input data for each class.

You will look at each now.

##### the class ellipse on a scatter plot

- From the Tools menu in the Training Site Editor select Scatter Plot

![](./img/m06-25.png)

![](./img/m06-26.png)

In the scatter plot window make sure the x-axis is set to 3 and the Y-axis is set to 4.

- In the bottom of the scatter plot, display the mean and plot ellipse for all four classes by clicking in the cells to check on

![](./img/m06-27.png)

You should notice ellipses of the class color appearing in the scatter plot in the top portion of the dialog (zoomed partial scatter plot image below). You may need to check on and off to get them to appear.

![](./img/m06-28.png)

If your ellipses do not overlap carry on.

##### Testing Signature Separability

- From the Training Sites Editor select Tools -> Signature Separability. The Signature Separability dialog opens and displays two tests of separability.

![](./img/m06-29.png)

- Click on the context sensitive help button on the lower left of the dialog (the book with question mark) to open the help. Read about the two tests.

![](./img/m06-30.png)

![](./img/m06-31.png)

Are your separability statistics good? – they should be perfect ( value of 2) as the ellipses DO NOT in any way overlap.

- Close the dialog when done.

##### View Signature Statistics

- From the Training Sites Editor select Tools -> Signature Statistics to open the Signature Statistics dialog.

![](./img/m06-32.png)

The General tab displays the ‘general’ statistics of your classes i.e. the mean, standard deviation and number of samples (pixels) used to calculate the statistics. You can also view matrix reports these are advanced options that we are not using for this tutorial or course.

- Look at the mean and standard deviation for each of your classes, to view these values select the class in the upper part of the dialog (click on the ID and notice the red rectangle), the values should be different for each class. Are yours?

- You can save the Signature statistics to a text file with the Save Report option.

- Open the report you saved in a text editor and look at it. Notice the mean and standard deviation (and matrix – not used at this time) information is saved.

- Close the signature statistics dialog when done.

##### View the histogram for the Training Class

You can view the histogram for your training sites for each input dataset. You are looking for a uni-modal histogram (as close as you can get). A class is a grouping of ‘like’ values.

- From the Training Sites Editor select Tools -> Histogram. A histogram dialog opens displaying the histogram for the input data sets (in this case ETM3 and 4) for the selected class in the Training Sites Editor dialog.

![](./img/m06-33.png)

- Look at the histogram are they uni-modal? You may need to change the maximum percentage shown to ~50%

- Select a different class and look at the histograms. Again are they uni-modal?

- Look at all your classes.

- Close the histogram dialog when complete.

You have looked at some tools to assess how good your training sites are. In this case yours should be very good and we only have 2 images and 4 very distinct classes.

When performing a classification you will most likely need to EDIT the training sites.

In this tutorial you do not need to. 

##### Preview the classification

- From the Training Sites Editor select Tools -> Classification preview -> select one of the classification algorithms and view the results in the Focus display area. The colors are the colors selected from your training sites.

- Try some of the other classification algorithms.

- From the Tools -> classification preview ->Select Show Training sites as your final option.

- Once you have finished Save and Close the Training Sites Editor.

After evaluating the training sites if the class ellipses overlap (badly), if the signature separability values are bad, if the mean/standard deviation overlay and/or if the histograms are multi modal then you should edit the training sites by deleting/adding other areas for each class. Then re-evaluate. The process continues until you are ‘satisfied’ with the classification. Your training sites should NOT be large. Large training sites can cover many classes. You can make training sites from LINES, POLYGONS and ANY OTHER SHAPE YOU DESIRE. This tutorial only showed rectangles, you are not limited to rectangles.

Now that you are satisfied with your training sites you will classify the image.

##### Classify the image

- Right-click on the Classification MetaLayer in the Maps tree of Focus and select Run Classification.

![](./img/m06-34.png)

- Select Parallelpiped for the Algorithm: with Maximum likelihood as tie breaker. Under the Classification Options select Show report, save signatures and create PCT (image below).

![](./img/m06-35.png)

- Select Ok when done.

If you receive the message file has changed reconfigure? Yes or No click YES

After classification a report appears.

![](./img/m06-36.png)


- Look at and save the report into your working directory mod06 folder.

- Look at the Output of the classification, open the legend (click on the + next to output) to assist in interpreting the colors in the output.

- Quit FOCUS. You do not need to save a Project (gpr) file.

##### Display classification results.

- Start Focus and add your classified image as a pseudo color layer (should be in channel 8 in the l7_rf_nvan database).

- Go to the files tab and your should see two new segments in your database. A pseudocolor section with a classification PCT and a signature section with four segments.

![](./img/m06-37.png)

- Rt-Click on the Grass signature and VIEW. Notice the stats for the classification and the class. Encoding: 1 is the DN for the grass class.

![](./img/m06-38.png)

![](./img/m06-39.png)

##### Create a thematic map

- Filter the pseudo color layer with a 3x3 and a 5x5 mode filter – apply to view only.

- Apply the 5x5 mode filter to your file. Save the filtered classified image to a new channel (make sure you give a new name and don’t overwrite the original classified image). Should be channel 9 make sure to give it a useful name.

##### Calculate the area of each land cover class.

- From the Algorithm Librarian find and open the AREAREPORT algorithm. Input your filtered image under the input params 1 report in hectares and send the report to LOG.

![](./img/m06-40.png)

![](./img/m06-41.png)

![](./img/m06-42.png)

- Look at the report. You should see the area of each class in hectares (scroll all the way to the right).

![](./img/m06-43.png)

It reports the area per DN. Remember you assigned the DN value to a class.

- You can copy and paste this report to a text document (ctrl-a select all ctrl-c copy then move to notepad and ctrl-v paste.)

- To make the report useful enter the ‘names’ of the class in the legend. Notice on ly NULL class is filled in. You know the names because you created them – it is also in the signatures.

##### Convert your raster image to vector polygons.

- From the Algorithm Librarian find and open the RAS2POLY (Convert a raster layer to a polygon layer) algorithm.

- Set the parameters as

Files Tab:
Input Ports
Input: Raster Layer = your 5x5 filtered classified image (should be in channel 9)
Output Ports
Output: Polygon Layer = viewer AND your l7_rf_nvan.pix database - Don’t forget to select output to the l7_rf_nvan.pix database and give your polygon layer a name.

- Switch to Log view and Run

- Look at the polygons generated zoom in to see the difference between raster and vector representation.

- Look at the attributes generated for the polygons (rt click on the TopoPoly: Topo Area Layer -> attribute manager). Your numbers will be different.

- The PixelValue is the same value as the DN from your classified image, it was set in the creation of training areas. The value corresponds with your land cover class, with the exception of 0 this is the area where no class was assigned.

##### Convert to Shapefile format.

- From the files tab rt click on the TopoPoly: TopoAreaLayer and select Export(save as) -> to new file.

- In the Translate (Export) File dialog fill in the parameters as followes:

Destination file: = <path to your working directory>LCVANCOUVER
Output format: = SHP:ArcView Shapefile
Options = POLYGON
Source Layers: select the TopoPoly: TopoAreaLayer segment (should be segment 15 OR 16) and >ADD> to the destination layers area.

- Hit Translate when done hit close.

- Use Focus to Open the shapefile you just created to view the data. File -> open -> select the LCVANCOUVER.SHP file.














