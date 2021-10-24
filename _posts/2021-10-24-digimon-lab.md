---
layout: post
title: Digimon Lab
subtitle: By Tuhin Ghosh
tags: [digimon]
comments: true
---

Collaborators: Claire Goldberg, Bulyn Panjamapirom, Darson Chen, Elias Romero, Uddipto Nandi, Divya Ponda, and Larry Tao

### 1. What is the average speed (Spd) of all Digimon?

This problem was quite easy as it just required iterating through the data, taking the speed of each, and maintaining a counter to divide by for the average. The one thing that I learned was that all of the data is stored as strings. Therefore, to add all of the speed values, I had to use the float() function to convert the string values of speed into numbers. 
That looked like:

```python
speed = float(digimon["Spd"])
```
This also let me divide the sum by the counter to get the average.

### 2. Write a function that can count the number of Digimon with a specific attribute. For example, count_digimon("Type", "Vaccine") would return 70.

This problem also required a counter, but instead of being able to define a variable as a specific column of each row, I had to make the name of that general. The name of that column would be the first parameter of the function which I was able to do as just:


```python
def count_digimon(Attribute, Specific_Value):
        counter_of_digimon = 0
        for digimon in data: 
            if(digimon[Attribute]==Specific_Value):
                counter_of_digimon+=1
```
As one can see, the if statement uses both parameters to make sure that the function can be run for any category and any value. 

### 3. The Digimon on your team are restricted by the total amount of Memory that they need. If your team only has 15 Memory, name a team of up to 3 Digimon that has at least 300 attack (Atk) in total.

For this question, I made a dictionary that had 3 values, '1', '2', and '3'. For each of these the values would be a dictionary of the set of groups of the size of the key that satisfied these conditions. The keys of this new dictionary are 'Group n' such that the corresponding value group would have been the nth group found by the code. I also included keys of 'Group n Memory to Attack Ratio' to allow comparisons between groups. I was able to define the key as 'Group n' through this code which involves a counter of the number of valid groups:

```python
dict_of_groups_of_3[("Group " + str(number_of_valid_groups_of_3))] = [digimon_name_1, digimon_name_2, digimon_name_3]
```
The variable number_of_valid_groups_of_3 is that counter. 

Another element of completing this problem was making sure that there were no digimon that were repeated. I did this through including all of the code to check if the group was correct in if statements that ensured there were no repeats. 

The one big problem I ran into was being able to access this dictionary without having to create it every single time. The code runs through nearly 2,000,000 combinations of digimon which takes a while and returns 100,000+ valid groups. So, I needed a way to export the dictionary so that I could access it with a separate file. I did this using the pickle module. The code looked like:

```python
the_dict = {}
the_dict = team_of_3(data)
a_file = open("File_for_the_dictionary", "wb")
pickle.dump(the_dict, a_file)
a_file.close()
```

This allows the dictionary file to be exported anywhere and opened with similar code. It is a very effective method to move my file around and not have to run the code extensively. 
