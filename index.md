# hello!

***Wellcome to my page!***
![meme](https://user-images.githubusercontent.com/102137136/159832470-cc577a22-eedd-4d61-87d0-93ebb63c9eeb.png)

## Cat is qute!

This cat is really qute, and that's why I make this picture by using R code and {magick} package.

## About code

**here's my code to make this picture:**

library(magick)


pict <- image_read(path = 'https://i.guim.co.uk/img/media/26392d05302e02f7bf4eb143bb84c8097d09144b/446_167_3683_2210/master/3683.jpg?width=1200&height=1200&quality=85&auto=format&fit=crop&s=49ed3252c0b2ffb49cf8b508892e452d')

temp <- image_blank(width = 1000,

                          height = 1000,
                          
                          color = '#FFFFFF') %>%
                          
  image_annotate(text = 'Quuuute Cat',
  
                 color = '#999999',
                 
                 size = 60,
                 
                 font = 'impact',
                 
                 gravity = 'center')
                 
library(magick)

meme <- image_append(c(pict, temp))

image_write(meme, 'C:/Users/NPC6/Downloads/meme.png')
