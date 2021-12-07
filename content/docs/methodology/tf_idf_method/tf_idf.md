---
title: "TF and TF-IDF"
---

# TF and TF-IDF



According to [Wiki](https://en.wikipedia.org/wiki/Tf%E2%80%93idf), there is a variaty of ways to calculate TF-IDF. We calculate TF-IDF in what appears to be the most conventional way, where the raw count, {{< katex >}} f_{t,d}{{< /katex >}} , of term {{< katex >}}t{{< /katex >}} in document {{< katex >}} d{{< /katex >}}  is standardized/adjusted by the document length, {{< katex >}} \sum_{t'\in{d}}f_{t',d}{{< /katex >}} , e.i. adjusted by the raw count of all the terms, {{< katex >}} t'{{< /katex >}} , in {{< katex >}}d{{< /katex >}} . Thus, {{< katex >}}TF(t,d){{< /katex >}}  becomes the share of words in {{< katex >}}d{{< /katex >}} that is {{< katex >}}t{{< /katex >}}. The equation for the standardized raw count (term frequency) is:
{{< katex display >}}  
TF_{t,d}=\frac{f_{t,d}}{\sum_{t'\in{d}} f_{t',d}}
{{< /katex >}}  
    
 Further, we use the inverse document frequency, IDF, to diminish the weight of terms that occur frequently across all documents and increase the weight of terms that are unique to a few documents. IDF is calculated as: 
{{< katex display >}}  
idf(t,D)=log\left(\frac{N}{\{d\in{D}:t\in{d}\}|}\right)
{{< /katex >}}  
       
 where {{< katex >}}N{{< /katex >}} is the number of documents, and {{< katex >}}{\{d\in{D}:t\in{d}\}|}{{< /katex >}} is the number of documents the term {{< katex >}}t{{< /katex >}} appears in (As our vocabulary is based on the words of the documents, we do not need to worry about a scenario where a term doesn't appear in any of the documents, which would otherwise  result in a division by 0). 
 

TF-IDF is simply the product of TF and IDF:
{{< katex display >}} 
TFIDF(t,d,D) = TF\bullet idf
{{< /katex >}}      

Thus, if a term appears in all the documents, its weight in all the documents will be reduced to 0, as:  
{{< katex display >}}
\frac{N}{|\{d\in{D}:t\in{d}\}|} = 1 \rightarrow IDF=log(1)=0
{{< /katex >}}

Further, if a term does not appear in a document, its weight in that document will also be reduced to 0, as {{< katex >}}f_{t,d}=0{{< /katex >}}. On the other hand, a high weight in TF–IDF is reached by a high term frequency (in the given document) and a low document frequency of the term in the whole collection of documents.

[Back to the TF-IDFs](/docs/Analysis/text_analysis/tf_idf_field/)