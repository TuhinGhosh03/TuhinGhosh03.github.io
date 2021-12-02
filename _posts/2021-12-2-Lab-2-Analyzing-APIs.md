---
layout: post
title: Lab 2 Analyzing APIs
subtitle: By Tuhin Ghosh
tags: [lab]
comments: true
---

### Collaborators: Larry Tao, Bulyn Panjamapiron, Elias Romero

## 1. Discuss how you used the API to obtain the dataset.

Since I had to create a new csv, I needed to iterate through the API and get the corresponding information for my dataset. To do that I used a while loop with the condition of 
the response I get from the request is not an error. This ensured that the size of the API could change, but my code would still work. Firstly, I had to define the response before the while
loop to satisfy the condition. This line and a line to set the row number of the API that was requested to 0 were the only ones(and some modules) before the while loop. Then, I defined the 
base url, endpoint, and api key based on the API's documentation. I also initialized a payload that contained the key and the aforementioned row number. Due to certain issues with my computer,
I had to encode the response the code recieved and then decode it as well to ensure that I could use it later. I used the codecs module and this code:

```python
response = requests.get(BASE_URL+ENDPOINT, params=payload)
unclean_data = response.text.encode()
actual_data = codecs.decode(data, encoding="utf-8-sig")
```
I then printed actual_data, so it could be redirected into a csv, and the row number was incremented by one.

## 2. Which sock has the most variations? If there is more than one answer, then list all of them.

argyle crew socks, color-blocked socks, frilly knee-high socks, holey tights, kiddie socks, mixed-tweed socks, no-show socks, semi-opaque socks, semi-opaque tights, sequin leggings, simple-accent socks, 
striped socks, striped tights, tube socks, ultra no-show socks, vivid leggings, vivid socks, and vivid tights all had the greatest number of variations at 8.

## 3. How many socks of each color are there? If a sock has two different colors, it should be counted in both. However, if a sock has the same Color1 and Color2, make sure you don’t double count it!

|Color|# of socks with the Color|
|-----|-------------------------|
|Pink|41| 
|Red|39|
|Green|50| 
Light blue| 33
Orange| 27
Purple| 37 
Blue| 47 
Yellow| 33 
Beige| 15 
White| 85 
Black| 59 
Brown| 11 
Gray| 31 
Colorful| 14

## 4 Discuss your process of how you worked on this lab. Include details such as who you worked with, what methods you tried, what worked or didn’t work, what could have gone better, and what you learned during this lab. Focus more on the programming side of the lab! Feel free to attach images, screenshots, pseudocode, etc to elaborate on your response.


