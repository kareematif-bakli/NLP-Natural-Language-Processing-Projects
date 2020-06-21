##  Word analogy task
"a is to b as c is to __".

An example is:
'man is to woman as king is to queen' .

We are trying to find a word d, such that the associated word vectors  ea,eb,ec,edea,eb,ec,ed  are related in the following manner:
eb−ea≈ed−eceb−ea≈ed−ec 
We will measure the similarity between  eb−eaeb−ea  and  ed−eced−ec  using cosine similarity.

# 1 - Cosine similarity

To measure the similarity between two words, we need a way to measure the degree of similarity between two embedding vectors for the two words. Given two vectors $u$ and $v$, cosine similarity is defined as follows: 

$$\text{CosineSimilarity(u, v)} = \frac {u \cdot v} {||u||_2 ||v||_2} = cos(\theta) \tag{1}$$

* $u \cdot v$ is the dot product (or inner product) of two vectors
* $||u||_2$ is the norm (or length) of the vector $u$
* $\theta$ is the angle between $u$ and $v$. 
* The cosine similarity depends on the angle between $u$ and $v$. 
    * If $u$ and $v$ are very similar, their cosine similarity will be close to 1.
    * If they are dissimilar, the cosine similarity will take a smaller value. 

<img src="images/cosine_sim.png" style="width:800px;height:250px;">
<caption><center> **Figure 1**: The cosine of the angle between two vectors is a measure their similarity</center></caption>
