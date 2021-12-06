---
title: "Preprocess"
---
# Proprocessing the data

To construct this "community" of social scientists, we found inspiration by examining the Faculty of Social Science at Copenhagen University. The Social Science faculty have five overall departments: Sociology, Psychology, Economy, Anthropology, and Political Science. For each of these five categories we have a list of scientists on wikipedia. We used these five lists of scientists to find and all the scientists in our final dataset. After gathering all the names from the five lists, we then gather each individual scientists from wikipage. Thus our data gathering process has two parts: 1) get social scientists from each of the five lists, 2) gather each scientists wikipage. 

For cleaning and preprocessing the data we work with two datasets: One is an edgelist for constructing networks. And the second dataset is for text analysis on the theorists wikipages.  

If a scientist is mentioned on more than one list we classify them as being in a sixth category 'Multiple'. 

Below we go more in depth with each of the two steps and our choices in the following sections. 