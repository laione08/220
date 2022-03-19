```r
library(magick)

pic1 <- image_read("https://cdn2.vectorstock.com/i/1000x1000/90/41/cartoon-little-girl-studying-vector-22369041.jpg") %>%
  image_scale(500) 

first_text <- image_blank(width = 500, height = 500, color = "#ffffff") %>%
  image_annotate(text = "Expectation during zoom lectures", color = "#000000", 
                 size = 30, font = "Impact", gravity = "center")

pic2 <- image_read("https://thumbs.dreamstime.com/z/happy-cute-girl-sleep-study-class-vector-163825060.jpg") %>%
  image_scale(500)

second_text <- left_text <- image_blank(width = 500, height = 300, color = "#ffffff") %>%
  image_annotate(text = "Reality", color = "#000000", 
                 size = 40, font = "Impact", gravity = "center")

first_row <- c(first_text, pic1) %>%
  image_append()

second_row <- c(second_text, pic2) %>%
  image_append()

meme <- c(first_row, second_row) %>%
  image_append(stack = TRUE)

image_write(meme, "my_meme.png")
```

<img src="my_meme.png" width="500" height="500"> 


### This meme was inspired by the university’s current learning environment in response to the uncertainty that covid 19 outbreaks come with. It is of course *not* an actual depiction of what happens in reality during zoom lectures. It is an adaptation of other expectations vs reality memes on the web that are intended to be humorous. 

#### Here are two relatable *expectation vs reality* memes: 

1. 
![Meme1](https://www.memesmonkey.com/images/memesmonkey/5d/5d941e63fa6d0b3afc9ab52411158248.jpeg)


2. 
![Meme2](https://i.pinimg.com/originals/e4/38/cb/e438cbf2ecf7b9cd9f2beedf81afc37d.jpg)


### On a slighty more serious note, here are a few websites with some tips on how to stay focused with studying despite the difficulty of the online learning environment: [**Host**](https://host-students.com/study-tips-for-students/), [**freedom**](https://freedom.to/blog/how-to-stay-focused-studying/) and [**wikiHow**](https://www.wikihow.com/Focus-on-Studying).

## **References**

"pic1", VectorStock, https://cdn2.vectorstock.com/i/1000x1000/90/41/cartoon-little-girl-studying-vector-22369041.jpg

"pic2", VectorStock, https://cdn2.vectorstock.com/i/1000x1000/90/41/cartoon-little-girl-studying-vector-22369041.jpg

"Meme1", Memes Monkey, https://www.memesmonkey.com/images/memesmonkey/5d/5d941e63fa6d0b3afc9ab52411158248.jpeg

"Meme2", TheMetaPicture, https://i.pinimg.com/originals/e4/38/cb/e438cbf2ecf7b9cd9f2beedf81afc37d.jpg
