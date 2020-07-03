# Project-2


rmarkdown::render("/Users/christinemarieheubusch/Project-2/Project 2 - ST 558 - CM Heubusch.Rmd", output_file="test123.html", params=list(day=c("Monday","Tuesday","Wednesday", "Thursday", "Friday", "Saturday", "Sunday"))


dayWeek <- newsData %>% select(starts_with("weekday_is_"))
output_file <- paste0(dayWeek, ".md")
params = lapply(dayWeek, FUN=function(x){list(day=x)})

#Placing the params list into a dataframe - each element within each column will be a list.
reports <- tibble(output_file, params) 
#The first column in the resulting tibble is the output file; the second is the list with one item in it.

library(rmarkdown)
apply(reports, MARGIN=1,
          FUN=function(x){
              render(input="/Users/christinemarieheubusch/Project-2/Project 2 - ST 558 - CM Heubusch.Rmd",   
              output_file=x[[1]], params=x[[2]])
          })
