---
# Do not edit the text between these lines!
layout: default
---

# COMP110 Exercise 09 -- Data Analysis for Continuous Improvement


<!-- This is a comment. Below, you'll see code for inserting an image. To make this image appear, update <custom-path>. To add an image, save it inside the imgs folder of this repository. -->

## Our Idea

The idea we chose to analyze was whether students should frequently create their own code examples when they are stuck because and if it may lead to stronger understanding of COMP110 material.

This idea is very practical as it requires no extra work for professors or TAs, the course does not need to be redesigned or taught differently. This idea is simply in the hands of teh students. It offers a way for students to take learning into their own hands and amke an immediate change themselves.

## Summary of Analysis
We first read the survey data using the read_csv_rows function which gave the original row-based version of the CSV file. Then we converted the row-based data into columns using the columnar function and previewed the first few rows of the dataset using the head function. Then to control for only the necessary functions we used the select function to only use "own_examples" and "understanding". Then we used the count function to see the distribution of responses for both variables. This made it easy to see how many students chose each rating. Then we made a helper function titled filter_by_threshold that filtered the data to only include students whose "own_examples" score was at or above a set threshold (which was 5 or more in this case). This represents the dataset of students who frequently create their own examples. Then, to analyze whether frequent example users reported stronger understanding we calculated the average understanding score for all students and compared it to the average understanding score for students who frequently create their own examples. The average understanding for students was 4.199 while the average understanding for frequent example users was 4.538. 

## Line Graph
<img src="static/line graph.png" alt="Image3" width="500"/>

In this graph the x axis represents the number of own examples while y represents understanding. This graph shows a positive trend, as students create more example their understanding increases. The line consistently increases apart from a slight dip around 3 examples.

## Dot Plot
<img src="static/dot plot.png" alt="Image2" width="500"/>

In this plot darker squares represent a higher concentration. This graph has darker squares around the middle ranges meaning 4-5 examples and 4-6 understanding, meaning most students cluster in moderate effort and moderate understanding.

## Heat Plot
<img src="static/image1.png" alt="Image1" width="500"/>

This plot shows individual data points without any averaging. It shows that points are spread across all combinations but denser around middle/high values. There are fewer points of low understanding when one's own examples are high. This shows that variability just exists but higher example counts tend to avoid low understanding scores. 


## Our Conclusion

This analysis explored if students create their own code examples and have a higher understanding of COMP110 materials. 
The data analyzed provides moderate support for this claim. Students who frequently created their own examples, which was defined during the analysis as a score of 5 or higher, had an average understanding score of 4.54, when compared to all students who had a 4.20 average score. 

This outcome suggests that students who generate their own examples tend to report high understanding on average. All three visualisations show that as frequency of own examples created increases, so does understanding scores, though not perfectly. Based on this analysis our recommendation is to encourage students to create their own examples when feeling confused about concepts. This strategy is low-cost and does not require any changes to the course content or structure, thus making it an easily implementable tool. The data, however, does have its limitations as it is self-reported by students making it subjective. Furthermore the relationship observed is purely correlational, thus we cannot conclude any causation. 

There are many other factors that could serve as explanation for the outcome. In the future, this analysis could be strengthened by incorporating performance-based metrics to strengthen the correlation. The potential trade offs are tied to student motivation or time. Some students might not have the time to go out of their way to create their own examples or find it frustrating/too difficult.
