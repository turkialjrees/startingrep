# startingrep
R Markdown interactive using Shiny.



This R Markdown document example is made interactive using Shiny. 
Unlike the more traditional workflow of creating static reports, you can now create documents that allow your readers to 
change the assumptions underlying your analysis and see the results immediately. 

#Run by single file only 
you can name the file YourNAme.Rmd


# you need to render a table such
renderTable({
  head(cars, input$rows)
})



To learn more, see [Interactive Documents](http://rmarkdown.rstudio.com/authoring_shiny.html).

## you need Inputs and Outputs

You can embed Shiny inputs and outputs in your document. Outputs are automatically updated whenever inputs change.  
This demonstrates how a standard R plot can be made interactive by wrapping it in the Shiny `renderPlot` function. 
The `selectInput` and `sliderInput` functions create the input widgets used to drive the plot.


## You can  Embedded Application

It's also possible to embed an entire Shiny application within an R Markdown document using the `shinyAppDir` function.
This example embeds a Shiny application located in another directory:

```{r tabsets, echo=FALSE}
shinyAppDir(
  system.file("examples/06_tabsets", package = "shiny"),
  options = list(
    width = "100%", height = 550
  )
)
```
