---
title: "Datasets"
---
# **Data**

Here we have the datasets which we have used for the project.
## The Wikipedia Lists
Here we link to the five social science lists, which our project is build upon.

{{< columns >}}

- [Sociologists](https://en.wikipedia.org/wiki/List_of_sociologists)

- [Psychologists](https://en.wikipedia.org/wiki/List_of_psychologists)

- [Political Scientists](https://en.wikipedia.org/wiki/List_of_political_scientists)

- [Economists](https://en.wikipedia.org/wiki/List_of_economists)

- [Anthropologists](https://en.wikipedia.org/wiki/List_of_anthropologists)

<--->
<left>
<img src="https://i.giphy.com/media/3oKIPpFhwsMNrRIjN6/giphy.webp" width=400 height=220>
</left>
{{< /columns >}}

Here we have the different datasets which we used for the project. To load the data into python, we suggest you use the following code-snippet:

```tpl
import requests
data = requests.get(dataset_url).json() 
```
Note that all of the datasets are in a json/dictionary format.

## Network Data

- [Edgelist](https://raw.githubusercontent.com/EsbenBL/social_graph_exam/main/edge_list.json)

- [Nodelist](https://raw.githubusercontent.com/EsbenBL/social_graph_exam/main/node_list.json)

- [Dictionary of the scientists and their field](https://raw.githubusercontent.com/EsbenBL/social_graph_exam/main/inv_science_name_dict.json)

- [Scientists, their field, and network community](https://raw.githubusercontent.com/EsbenBL/social_graph_exam/main/name_field_community.json)

## Text Data

- [Cleaned Wikipedia content](https://raw.githubusercontent.com/EsbenBL/social_graph_exam/main/wiki_dict_noname.json)

## HSBM Data

For a more indepth rundown of the data cleaning process, the code is available in following [this link to a ipynb-notebook](https://github.com/EsbenBL/social_graph_exam/blob/main/Explainer_notebook.ipynb)

