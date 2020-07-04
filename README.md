<<<<<<< HEAD
# Project-2

library(tidyverse)

for ({
unique(select(starts_with("weekday_is_*")==1)

}

rmarkdown::render(input="/Users/christinemarieheubusch/Project-2/Project 2 - ST 558 - CM Heubusch.Rmd",
  params=list(day=dplyr::select(starts_with("weekday_is_"))),
  output_format=".md",
  output_file=paste0(gsub(".md","", day), ".md"))


## Getting unique columns
dayWeek <- newsData %>% unique(select(starts_with("weekday_is_*")==1))
output_file <- paste0(dayWeek, ".md")
params = lapply(dayWeek, FUN=function(x){list(*=x)})

#Placing the params list into a dataframe - each element within each column will be a list.
reports <- tibble(output_file, params) 
#The first column in the resulting tibble is the output file; the second is the list with one item in it.

library(rmarkdown)
apply(reports, MARGIN=1,
          FUN=function(x){
              render(input="/Users/christinemarieheubusch/Project-2/Project 2 - ST 558 - CM Heubusch.Rmd",   
              output_file=x[[1]], params=x[[2]])
          })
=======
## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/cmheubus/Project-2/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/cmheubus/Project-2/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
>>>>>>> 39a56e950019c64d069e80cc571aa9139e0d99cc
