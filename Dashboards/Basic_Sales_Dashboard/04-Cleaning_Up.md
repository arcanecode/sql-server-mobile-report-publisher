# Cleaning Up the Dashboard

In this section we'll go through the various elements on the dashboard, as well as the dashboard itself, and add the finishing touches to make it look like a completed, professional report.

First, you obviously need the report open in Mobile Report Publisher. Then make sure you are on the _Layout_ tab.

If you've not done so, click in the top area and rename the report to **Sales Dashboard**.

## Category Chart

Click on the Category Chart report element. At the bottom you will see the properties for this element.

Change the title to **Sales by Year**.

One other optional change that may be useful to this report. By default the chart's Y axis starts at 0. Since we are dealing such large values, it may be useful to start the Y with a higher value. This will make it easier to see variations between years.

To do so, click the _Adjust Y range to values_ slider. You should see the chart element update with a higher Y axis.

## Bullet Graph

Next, click the Bullet graph to edit its properties. Start with the Title, setting it to **Sales YTD**.

Now move to the Subtitle right below it, and enter **vs Previous YTD**.

Now let's look at the ranges for how the bullet graph displays the red/yellow/green values. Click on the **Set ranges** button.

Right now the current value is sales to date for the current year. We want to compare it to the sales to date for the same period last year. By default, if our current sales exceeds 100% of last years sales, the bullet graph shows green.

If current year sales are between 75 and 100 percent, it is marked as neutral, or yellow. Below 75 percent is bad, and is marked with red.

We won't change them for this demo, but you should be aware of where the can be changed, how they function.

## Simple Data Grid

Click on the Simple data grid, then go down to the Visual properties.

Click in the title field, and remove what is there. That's it, for this grid we're going to leave the title blank. In this case, it is quite obvious this is sales by year and state.

For this demo, we're just showing that the title is not a required field, if it makes sense you can leave it empty.

In this report, row numbers won't be very helpful, so we'll turn them off. Scroll to the right, and change the **Row numbers** to **Hide**.

## Gradient Heat Map

Shifting to the Gradient heat map, start by changing its title to Sales by State. In the subtitle, put **Cumulative**.

In a later report we'll show how to limit this to a particular year, but for now we'll just let it show the cumulative total for all years.

We won't change anything else, but do note that the Map field gives you access to a wide array of maps, should you be operating on another part of the planet, or across the entire world.

## Tree Map

Finally we get to the Tree map. Change the title to **Sales by Year and Territory**. The remaining values can remain unchanged.

## Previewing the Results

Save your report, then click the Preview button to see the results.

Scroll down in the simple data grid to see its values.

Next, shift to the gradient heat map. Click on a state, and hold down the mouse button. When you do, a pop up will appear with the name of the state and the value.

Now move to the tree map. Click on one of the year labels to expand that year to take up the entire area. When you do, you should see the pop up text appearing in the box.

Click on the year to zoom back out to the entire dataset. Now click and hold, as you did with the tree map, in one of the squares. A pop up will appear with the data for that square.

Do note you can use the click and hold pop up feature no matter how far down into the tree map you've drilled.

## Conclusion

From here, we are ready to design the dashboard for a tablet. You'll learn how in the next file, [05-Tablet.md](05-Tablet.md)
