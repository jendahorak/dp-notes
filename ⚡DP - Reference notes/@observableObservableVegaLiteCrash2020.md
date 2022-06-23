---
title: Observable VegaLite A Crash Course
authors: 
year: 2019
---

url:  https://www.youtube.com/watch?v=ZV_Yjcs5WtM
zot: [See in Zotero](zotero://select/items/@observableObservableVegaLiteCrash2020)
status:
# Observable: Vega-Lite: A Crash Course

# What is it
D3 - Vega - Vega-Lite

``` js
import { vl } from "@vega/vega-lite-api"

vl.markCircle()                        // Make a scatter chart
  .data(cars)                          // Using the cars data (below)
  .encode(
    vl.x().fieldQ("Horsepower"),       // For x, use the Horsepower field
    vl.y().fieldQ("Miles_per_Gallon"), // For y, use the Miles_per_Gallon field
    vl.tooltip().fieldN("Name")        // For tooltips, show the Name field
  )
  .render()


```




# Resources
https://observablehq.com/@observablehq/vega-lite?collection=%40observablehq%2Fobservable-for-vega-lite
