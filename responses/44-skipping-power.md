#### Check your progress

_Copy your console output from the `tar_make()` you just ran_

Do you get something like this, where only four targets were rebuilt?

```r
v skip target oldest_active_sites
v skip target nwis_data_MI
v skip target nwis_data_IL
v skip target nwis_data_MN
v skip target nwis_data_WI
v skip target site_map_png
v skip target tally_MI
* run target timeseries_png_MI
  Plotting data for MI-04063522
* run target timeseries_png_IL
  Plotting data for IL-05572000
v skip target tally_IL
v skip target tally_MN
* run target timeseries_png_MN
  Plotting data for MN-05211000
v skip target tally_WI
* run target timeseries_png_WI
  Plotting data for WI-04073500
* end pipeline
```

_Copy ... one of the updated plots as a comment on this issue_

I edited `ggtitle(site_data$Site[1])` to be `ggtitle(sprintf("%s-%s", site_data$State[1], site_data$Site[1]))`, so my updated plot looks like

![updated_wi_plot](https://user-images.githubusercontent.com/13220910/119910012-d1370c00-bf1b-11eb-926e-05c69be70837.png)

### :keyboard: Activity: Merge your new appliers

Now that we've added these new appliers and thoroughly tested them, your code is ready for a pull request. Go for it!

<hr><h3 align="center">I'll respond when I see your PR.</h3>
