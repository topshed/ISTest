## Visualising your data
There are four main display views in Initial State. Each one can be useful in Visualising and understanding your data in different ways.

### Source view

The **Source view** is a simple list of every data point uploaded to your bucket. This can be useful in debugging any problems with your upload and you can also export this list as a CSV file by clicking on the **Save As File** button.


### Lines view

Lines is an interactive, stacked line graph view. You can examine multiple numerical-based signals on a shared x and y axis. This makes it easy to measure time and magnitude differences and spot correlations between data.

![](images/image19.png)

You can zoom in on a particular region of the plot and measure the differences in values using the cursors (you can add a cursor from the Tools menu).
 
![](images/image20.png)

### Waves view

The Waves option is an interactive, multi-row waveform viewer. You can examine your data in more detail by zooming in/out, collecting targeted statistics, and moving signals around.

The type of data loaded determines how it is displayed. Numerical data is drawn as spark lines. Data with only two values that have a true/false connotation (e.g., up/down, open/closed) are drawn as bit signals.  String data is drawn as a digital string bus.

The default layout for the Waves view is for all data streams to be the same height.

![](images/image16.png)

You can make any single stream larger by selecting it so that it is highlighted and then clicking on the **Tools** menu item and choosing **Amplify Signal +**

![](images/image17.png)

The more times you click, the taller that stream's plot will become.

![](images/image18.png)

For data that can be represented as a string, such as the Wind Direction, the **Signal Stats** option, available from the *Stats* menu item is a great way of seeing how much time the data has been a particular value.

![](images/image15.png)
