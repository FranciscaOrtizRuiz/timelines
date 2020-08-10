---
title: "Timelines"
author: "Francisca Ortiz"
date: "8/10/2020"
output: html_document
---

## I. Timeline to represent big stages 

A good example of this, it is the representation of the stages in a research. In this case, it is represented four big stages of my PhD thesis research: Theoretical frame, Fieldwork, Analysis and Writing. Something benefitial of using this package is it allows a simple and comfortably visual with a simple code. 

**Firts, load the package "vistime".**
```{r message=FALSE, warning=FALSE}
#install.packages("vistime")
library("vistime")
```

**Second, construct the data frame.**
```{r message=FALSE, warning=FALSE}
timeline_data <- data.frame(event = c("Theoretical frame", "Fieldwork", "Analysis", "Writing"), 
                            start = c("2018-09-01", "2019-09-01", "2019-12-01", "2020-01-02"), 
                            end = c("2019-09-01", "2020-01-15", "2020-10-01", "2021-09-01"), 
                            group = "Stages of 
                            the research")
```

**Third, select the better option for your research: static or interactive visualizations.**

A static option of the visualization:
````{r message=FALSE, warning=FALSE}
gg_vistime(timeline_data) 
```

An interactive option of the same visualization:
````{r message=FALSE, warning=FALSE}
hc_vistime(timeline_data)
```

There is another interactive option:
````{r message=FALSE, warning=FALSE}
vistime(timeline_data)
```

**Arguments of each function**

- **vistime**(data, col.event = "event", col.start = "start", col.end = "end", col.group = "group", col.color = "color", col.fontcolor = "fontcolor", col.tooltip = "tooltip", optimize_y = TRUE, linewidth = NULL, title = NULL, show_labels = TRUE, background_lines = NULL)

- **hc_vistime**(data, col.event = "event", col.start = "start", col.end = "end", col.group = "group", col.color = "color", optimize_y = TRUE, title = NULL, show_labels = TRUE)

- **gg_vistime**(data, col.event = "event", col.start = "start", col.end = "end", col.group = "group", col.color = "color", col.fontcolor = "fontcolor", optimize_y = TRUE, linewidth = NULL, title = NULL, show_labels = TRUE, background_lines = NULL)




