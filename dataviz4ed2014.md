---
title       : Data Visualization for Education
subtitle    : SDP Institute for Leadership in Analytics February 2014
author      : Jared Knowles
job         : Research Analyst, Wisconsin DPI
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : prettify  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : standalone # {standalone, draft}
---

## The Problem of Data Visualization

- Data use is increasing rapidly within the education space
- Policymakers are under increasing pressure to use data to inform decisions, 
justify funding, and guide practice
- **But,** policymakers are often **not** statisticians, researchers, or quants
- **Data visualization** is a way to bridge this gap
- Proper data visualization will bring the data to the audience in a way they can understand quickly and use to inform decisions

--- &twocol w1:50% w2:50%

## Follow Along

***left

### http://goo.gl/bhSzVJ

***right

<p align="center"><img src="img/knowleslogo.png"  style="display: block; margin:0 auto; height:auto; width:auto; max-width:350px; max-height:196px"></p>

--- &twocol w1:50% w2:50%

## What is dataviz?

***left
### Dataviz is...
>- An exploratory tool for understanding datasets
>- A communication tool for framing decisions and depicting problems
>- A way to showcase 
>- A better way to present results of analyses

***right
### Dataviz is not...
>- Easy
>- A replacement for analysis
>- Infographics
>- Easy!


--- quote

<p><q>Data visualization is a tool for communicating <span class = 'red'>a 
specific feature</span> of a datset in an approachable and efficient manner</q></p>

--- quote

<p><q>If a picture is worth a thousand words, a good data visualization must 
always be <span class = 'red'>better than a table.</span></q></p>

---

## Student Growth

<p align="center"><img src="img/stuplot25.png"  style="display: block; margin:0 auto; height:auto; width:auto; max-width:750px; max-height:560px"></p>


---

## Objectives

1. Review data visualization principles
2. Look at applications in education data
3. Best practices and advice
4. Review tools to use
5. Activity!




--- plot

## Example

How can we improve this simple scatterplot?

<img src="figure/plot.svg" title="plot of chunk plot" alt="plot of chunk plot" width="700px" height="500px" style="display: block; margin: auto;" />



--- &twocol w1:20% w2:80%

## Principles

*** left
- Elements of a chart
- Chart Types and Data Types
- Dimensionality
- Scale
- Complexity
- Technical details
- Beyond charts

*** right

<img src="figure/plot1.svg" title="plot of chunk plot1" alt="plot of chunk plot1" width="550px" height="330px" style="display: block; margin: auto;" />





---

## Chart Elements

There are a few things that all charts need [most of the time!]:  

- **Axis labels** and a **title**
  * These make the chart self-explanatory
- A **legend**
  * What is the unit in the graphic?
- A **scale**
  * How are units mapped to the visual space
- **Annotations**
  * Author and data source (depending on distribution)

> These add up to provide context and meaning to viewers who have not analyzed 
the dataset themselves.

---

## Dimensions

- Charts and data are made up of dimensions (e.g. a bar chart is *x* and *y*)
- Additional dimensions can be represented by additional aesthetics or chart 
elements (e.g. color, size, shape, etc.)
- Dimensions can also be shown by multiple plots (e.g. a filmstrip)
- **Smart use of dimensions allows us to increase the information density of our charts**


<img src="figure/unnamed-chunk-2.svg" title="plot of chunk unnamed-chunk-2" alt="plot of chunk unnamed-chunk-2" width="680px" height="300px" style="display: block; margin: auto;" />


--- quote

<p><q> How you turn dimensions in the <span class = 'red'>data</span> into visual 
cues for your audience is everything.</q></p>

--- quote

## Reviewing Chart Types

---

## Stacked Bar

<p align="center"><img src="img/d3stackedbar.png" height="550" width="800"></p>

--- 

## Box and Whisker

<p align="center"><img src="img/d3boxwhisker.png" height="490" width="700"></p>

---

## Bullet Chart

<p align="center"><img src="img/d3bulletchart.png" height="320" width="800"></p>

---

## Calendar

<p align="center"><img src="img/d3calendar.png" height="440" width="875"></p>

---

## Lines

<p align="center"><img src="img/d3linemany.png" height="440" width="875"></p>

---

## Parallel Sets

<p align="center"><img src="img/d3parallelsets.png" height="440" width="875"></p>

---

## Tree Map

<p align="center"><img src="img/d3treemap.png" height="470" width="950"></p>

---

## Word Cloud

<p align="center"><img src="img/d3wordcloud.png" height="420" width="900"></p>

---

## Data Types

- Any given dimension may be measured at different [levels of measure](http://en.wikipedia.org/wiki/Level_of_measurement) [derived by Stanley Smith Stevens in the 1940s and 50s]
  * Nominal: unordered categories of data (e.g. race)
  * Ordinal: ordered categories of data, relative size and degree of difference between categories is unknown (e.g. Likert scales, proficiency levels, etc.)
  * Interval: ordered categories of data, fixed width (e.g. grade level in school, GPA)
  * Continuous (ratio): a measurement scale in a continuous space with a meaningful zero (e.g. scale scores)

---

## Mapping Levels of Measure to Visual Cues

### Aesthetics for Mapping

How do we map levels of measurement onto visual features of charts?

Aesthetic |      Discrete              |  Continuous
----------|  ------------------------- | -------------------------------
Color     |  Disparate colors          |  Sequential or divergent colors
Size      |  Unique size for each value|   mapping to radius of value
Shape     |  A shape for each value    |   *does not make sense*

### Ordered vs. Unordered

Aesthetic  |    Ordered                         |  Unordered
---------- |  --------------------------------  |   -------------------------
Color      |  Sequential or divergent colors  |    Rainbow
Size       |  Increasing or decreasing radius |    *does not make sense*
Shape      |  *does not make sense*         |    A shape for each value

---

## Some tips

- Focus on the content and the context
- Know your audience, understand their limits, then push them!
- Use best practices, except when they don't help
- Experiment and iterate!

--- plot

## Charting Categorical Data

<img src="figure/unnamed-chunk-3.svg" title="plot of chunk unnamed-chunk-3" alt="plot of chunk unnamed-chunk-3" width="680px" height="480px" style="display: block; margin: auto;" />


--- 

## Charting Ordinal Data

<img src="figure/unnamed-chunk-4.svg" title="plot of chunk unnamed-chunk-4" alt="plot of chunk unnamed-chunk-4" width="750px" height="550px" style="display: block; margin: auto;" />


---

## Charting Interval/Continuous Data

<img src="figure/unnamed-chunk-5.svg" title="plot of chunk unnamed-chunk-5" alt="plot of chunk unnamed-chunk-5" width="750px" height="550px" style="display: block; margin: auto;" />


--- quote

<p><q> Think like a <span class = 'red'>map</span>. Data density and easy interpretability.</q></p>

--- map

## Maps

<p align="center"><img src="img/evenFRLmap.gif"  style="display: block; margin:0 auto; height:auto; width:auto; max-width:550px; max-height:600px"></p>

---

## Complexity

How do we display thousands or hundreds of thousands of observations with varying data types across multiple dimensions?

1. **Summarize the data**
  * Display summary statistics visually depicting the central tendency and spread of data
2. **Plot the raw data**
  * Annotate wisely to display the main message
3. **Model the data**
  * Use a statistical model to summarize features of the data

Let's look at some examples of this. 

--- 

## Summarizing Data

- The most simple summaries are measures of central tendency, most easily understood
- It is important to look at the spread of data too though
- If time is of interest, we are interested in trends
- If space is of interest, we are interested in maps or spatial distributions
- **Think about context and reference**
- Let's look at an example summarizing student data to schools!

---

## Plotting Means

Here is a simple plot of mean school reading scores:

<img src="figure/plotmeans.svg" title="plot of chunk plotmeans" alt="plot of chunk plotmeans" width="750px" height="500px" style="display: block; margin: auto;" />


But, what's wrong with this plot?

--- &twocol w1:20% w2:80%

## Mistakes

*** left

>- No sense of scale
>- Means can be skewed
>- Simple means are not meaningful
>- With assessment scores we need to know grade distribution
>- Let's try to improve this

*** right

<img src="figure/plotmeanssmall.svg" title="plot of chunk plotmeanssmall" alt="plot of chunk plotmeanssmall" width="400px" height="325px" style="display: block; margin: auto;" />


---

## Adding a Dimension

<img src="figure/meanplot2.svg" title="plot of chunk meanplot2" alt="plot of chunk meanplot2" width="750px" height="550px" style="display: block; margin: auto;" />


--- 

## Even More Dimensions

<img src="figure/meanplot3.svg" title="plot of chunk meanplot3" alt="plot of chunk meanplot3" width="750px" height="550px" style="display: block; margin: auto;" />


---

## Annotation

We still aren't sure what the mean scale score means. Let's see a couple more additions that can make this useful. 

<img src="figure/meanplot4.svg" title="plot of chunk meanplot4" alt="plot of chunk meanplot4" width="750px" height="480px" style="display: block; margin: auto;" />


---

## Caterpillar Plots

<img src="figure/catplot1.svg" title="plot of chunk catplot1" alt="plot of chunk catplot1" width="750px" height="480px" style="display: block; margin: auto;" />


---

## Raw Data

Sometimes, we can get away with showing the raw data, that is, all data points. We may want to do this for a few reasons:

- the "wow" effect, 
- because it is easier, 
- or because it looks better aesthetically. 

How could it be done?

---

## 600,000 Observations Too Many

<img src="figure/rawdata1.png" title="plot of chunk rawdata1" alt="plot of chunk rawdata1" width="750px" height="550px" style="display: block; margin: auto;" />


---

## Strategies for Presenting Big Data

- Without reducing the data points we need to do one or more of three things to 
be successful

1. Spread the data out
2. Bin the data into groups
3. Annotate and add references


---

## Spreading the Data Out

1. **Repeat the plot for subgroups**
  * Allow the viewer to draw comparisons across small plots
2. **Reduce the ink**
  * Each point has too much "weight", so make them weigh less
3. **Add Reference Points**
  * 600,000 observations in one panel is not meaningful and overwhelms the viewer

>- Edward Tufte and others recommend **small multiples**, a technique of repeating a plot across groups to compare relationships in multiple dimensions 

---

## What About This

<img src="figure/rawdata2.png" title="plot of chunk rawdata2" alt="plot of chunk rawdata2" width="750px" height="550px" style="display: block; margin: auto;" />


---

## Even Smaller Multiples

<img src="figure/rawdata3.png" title="plot of chunk rawdata3" alt="plot of chunk rawdata3" width="750px" height="550px" style="display: block; margin: auto;" />


---

## Binning Data

<img src="figure/rawdata4.svg" title="plot of chunk rawdata4" alt="plot of chunk rawdata4" width="750px" height="550px" style="display: block; margin: auto;" />



--- quote

## Modeling the Data

<p><q> All models are <span class = 'red'>wrong</span>. Some models are useful.</q></p>

---

## Smoothers 

<img src="figure/unnamed-chunk-6.svg" title="plot of chunk unnamed-chunk-6" alt="plot of chunk unnamed-chunk-6" width="800px" height="550px" style="display: block; margin: auto;" />


---

## Comparing Model Performance

<p align="center"><img src="img/EWSreview.png" style="display: block; margin:0 auto; height:auto; width:auto; max-width:700px; max-height:750px"></p>


--- 

## Aiding in Model Choice

<p align="center"><img src="img/EWSfull.png" style="display: block; margin:0 auto; height:auto; width:auto; max-width:700px; max-height:750px"></p>

---

## Regression Trees

<p align="center"><img src="img/parttree.svg"  style="display: block; margin:0 auto; height:auto; width:auto; max-width:700px; max-height:490px"></p>

---

## Regression Results

<p align="center"><img src="img/modelbracketlang.svg"  style="display: block; margin:0 auto; height:auto; width:auto; max-width:700px; max-height:490px"></p>

---

## Coefficient Comparisons

<p align="center"><img src="img/modelplot.png"  style="display: block; margin:0 auto; height:auto; width:auto; max-width:700px; max-height:550px"></p>

---

## Path Diagrams

<p align="center"><img src="img/pathdiagram.png"  style="display: block; margin:0 auto; height:auto; width:auto; max-width:700px; max-height:490px"></p>

---

## Illustrating a Model through Simulation

<p align="center"><img src="img/withinstudentplot.png"  style="display: block; margin:0 auto; height:auto; width:auto; max-width:700px; max-height:490px"></p>

---

## Simulating Outcomes

<p align="center"><img src="img/ELP_Survival_Curves_DRAFT.png"  style="display: block; margin:0 auto; height:auto; width:auto; max-width:800px; max-height:620px"></p>

---


## Combining Features

We can combine these features. 

>- Facets with smoother lines for references (small multiples + models)
>- Summary plots with raw data in the background
>- Reference lines and group comparisons

--- animation

## Animation Example

<p align="center"><img src="https://dl.dropbox.com/u/1811289/TESTstuplot.gif"  style="display: block; margin:0 auto; height:auto; width:auto; max-width:750px; max-height:550px"></p>

---

## Why does this work?

>- Annotation
>- Labeling
>- Lots of data-ink
>- Reference points galore

---
## Some tips

>- Have a properly chosen format and design 
>- Use words, numbers and drawing together
>- Reflect a balance, a proportion, relevant scale
>- Display an accessible complexity of details
>- Have a narrative quality, tell a story
>- Avoid content-free decoration (Tufte's proverbial chartjunk)
>- Draw in a professional manner with an eye on the technical details
>- Provide your audience with the context they need and remember they haven't 
lived in the data like you!

--- plot

## Themes
They can **communicate**, **confound**, **brand**, and **distract**

<img src="figure/plot21.svg" title="plot of chunk plot2" alt="plot of chunk plot2" width="400px" height="220px" /><img src="figure/plot22.svg" title="plot of chunk plot2" alt="plot of chunk plot2" width="400px" height="220px" /><img src="figure/plot23.svg" title="plot of chunk plot2" alt="plot of chunk plot2" width="400px" height="220px" /><img src="figure/plot24.svg" title="plot of chunk plot2" alt="plot of chunk plot2" width="400px" height="220px" />


---

## Technical Details


--- &twocol w1:50% w2:50%

## Graphics Files

*** left

### Raster
- Files like **jpg** , **png** , **gif**. 
- Fixed scale, aspect ratio, and size
- Reasonable file size
- Viewable in almost any image viewing and editing system, including any modern web browser, PowerPoint, etc.

*** right

### Vector
- Files like **pdf** and **svg**
- Infinitely zoomable, adjustable on the fly
- Larger file size
- Viewable and usable in fewer systems. SVGs can be used in modern web browsers. PDFs included in other PDF reports. 

---

## Technologies

The technology you choose to do visualizations is largely a question of personal productivity, but with some important caveats:

- In the future, more and more content is going to be delivered in a paperless world, so pick a technology that can leverage web/tablet/phone interfaces
- Different technologies are useful for different levels of finish and polish; Adobe Illustrator is great for publication quality graphics, R is a great tool for rapidly prototyping different visualizations
- Chose a technology that best serves your **consumer**, not you the producer. Charts are a service to the consumer, not to the creator. 

---

## Some Technologies

<img src="figure/technologies.svg" title="plot of chunk technologies" alt="plot of chunk technologies" width="750px" height="550px" style="display: block; margin: auto;" />


---

## Programming vs. Illustrating

Keep in mind that depending on the project you may need to programatically make 
data visualizations, or you may need a highly customized illustrated graphic. 

---

## Beyond Graphics

We have a number of other techniques we can use beyond simple charts. 

- Animations
- Interactive demos
- Summary tables
- Videos
- Web sites
- Simulations


--- &twocol w1:20% w2:80%

## Group Exercise

Visualize some education data. Imagine we have the following dimensions and want 
to present more of them on a plot like that on the right. Think about a story 
you might want to tell and then sketch out your result with your group.

*** left

- Grade
- Disability Status
- Type of Disability
- Language Proficiency
- School
- Math Score
- Reading Curriculum
- Math Curriculum

*** right

<img src="figure/studentexample.svg" title="plot of chunk studentexample" alt="plot of chunk studentexample" width="420px" height="350px" style="display: block; margin: auto;" />


---

## Example

<img src="figure/studentexample2.svg" title="plot of chunk studentexample2" alt="plot of chunk studentexample2" width="700px" height="500px" style="display: block; margin: auto;" />



---
## References

- Tufte, Edward. 1992. [The Visual Display of Quantitative Information.](http://www.amazon.com/The-Visual-Display-Quantitative-Information/dp/0961392142/) Graphics Press. 
- Unwin, Theus, and Hofmann. 2006. [Graphics of Large Datasets: Visualizing a Million.](http://www.amazon.com/Graphics-Large-Datasets-Visualizing-Statistics/dp/0387329064) Springer. 
- Wilkinson, Leland. 2005. The Grammar of Graphics. Springer.
- Ware, Colin. 2012. [Information Visualization: Perception for Design.](http://www.amazon.com/Information-Visualization-Third-Edition-Technologies/dp/0123814642/ref=reg_hu-rd_add_1_dp) 3rd Edition. Morgan Kaufmann. 
- Cleveland, William. 1994. [The Elements of Graphing Data.](http://www.amazon.com/gp/product/0963488414/) Hobart Press. 
- Cleveland, William. 1993. [Visualizing Data.](http://www.amazon.com/gp/product/0963488406) Hobart Press.

---

## References

- Few, Stephen. 2009. [Now You See It: Simple Visualization Techniques for Quantiative Analysis.](http://www.amazon.com/gp/product/0970601980/) Analytics Press. 
- Few, Stephen. 2012. [Show Me the Numbers: Designing Tables and Graphs to Enlighten.](http://www.amazon.com/gp/product/0970601972) Analytics Press. 
- Yau, Nathan. 2011. [Visualize This: The FlowingData Guide to Design, Visualization, and Statistics.](http://www.amazon.com/Visualize-This-FlowingData-Visualization-Statistics/dp/0470944889/) Wiley.
- Few, Stephen. 2006. [Information Dashboard Design: The Effective Visual Communication of Data.](http://www.amazon.com/Information-Dashboard-Design-Effective-Communication/dp/0596100167) O'Reilly Media

---
## Where to Learn Online?

- [Andy Kirk](http://www.visualisingdata.com)
- [D3](http://d3js.org/)
- [The Functional Art](http://www.thefunctionalart.com/)
- [ggplot2](http://www.ggplot2.org)
- [Robert Kosara](http://eagereyes.org/about)
- [Data Stories Podcast](http://datastori.es/)


--- &twocol w1:50% w2:50%

## Review of Key Concepts

***left

- Dimensionality
- Aesthetics and Mappings
- Small multiples
- Spreading the data out
- Web vs. print

***right

- Adapt and iterate
- Modeling the data
- Themes and style
- Techniques and software

---

## Contact Information

- DEWS Homepage: [http://wise.dpi.wi.gov/wisedash_dews](http://wise.dpi.wi.gov/wisedash_dews)
- E-mail: jared.knowles@dpi.wi.gov / jeknowles@wisc.edu
- GitHub: [http://www.github.com/jknowles](http://www.github.com/jknowles)
- Homepage: [www.jaredknowles.com](http://www.jaredknowles.com/)
- Google+: [https://plus.google.com/+JaredKnowles](https://plus.google.com/+JaredKnowles)


<p align="center"><img src="img/knowleslogo.png"  style="display: block; margin:0 auto; height:auto; width:auto; max-width:350px; max-height:196px"></p>

---

## For Fun

<p align="center"><img src="img/periodictablevisualization1.png" height="550" width="900"></p>

--- 

## Backmatter


```r
print(sessionInfo(),locale=FALSE)
```

```
R version 3.0.2 (2013-09-25)
Platform: x86_64-w64-mingw32/x64 (64-bit)

attached base packages:
[1] grid      stats     graphics  grDevices utils     datasets  methods  
[8] base     

other attached packages:
 [1] mgcv_1.7-28          nlme_3.1-113         plyr_1.8            
 [4] vcd_1.3-1            hexbin_1.26.3        lattice_0.20-24     
 [7] ggthemes_1.5.1       eeptools_0.3         MASS_7.3-29         
[10] ggplot2_0.9.3.1      knitr_1.5.15         slidifyLibraries_0.1
[13] markdown_0.6.4       whisker_0.3-2        slidify_0.3.3       
[16] devtools_1.4.1      

loaded via a namespace (and not attached):
 [1] abind_1.4-0        arm_1.6-10         car_2.0-19        
 [4] coda_0.16-1        colorspace_1.2-4   data.table_1.8.10 
 [7] dichromat_2.0-0    digest_0.6.4       evaluate_0.5.1    
[10] foreign_0.8-59     formatR_0.10       gtable_0.1.2      
[13] httr_0.2           labeling_0.2       lme4_1.0-6        
[16] maptools_0.8-27    Matrix_1.1-2       memisc_0.96-9     
[19] memoise_0.1        minqa_1.2.3        munsell_0.4.2     
[22] nnet_7.3-7         parallel_3.0.2     proto_0.3-10      
[25] RColorBrewer_1.0-5 Rcpp_0.11.0        RCurl_1.95-4.1    
[28] reshape2_1.2.2     scales_0.2.3       sp_1.0-14         
[31] splines_3.0.2      stringr_0.6.2      tools_3.0.2       
[34] yaml_2.1.10       
```

---



