---
layout: post
title: Fitch's Algorithm
---

Fitch's algorithm is a 2 pass algorithm:
1. Do postorder traversal. Store a set of characters at each internal node and root. Take an intersection of child nodes. If intersection is empty, take union.

2. Once the whole tree is populated, do preorder traversal, select the parent's label from child's character set. If there isn't any, select anything from the character set.

![an image alt text]({{ site.baseurl }}/images/fitch1.JPG "Fitch's Algorithm tree")

For instance, In the above tree, S3 will be {A,C}, S2 will be {A} and S1 will be {A,T} after pass 1.
In pass 2, we will arbitrarily select one of the character from root's character set, let's say A here. Then, we will check S2, the parent of S2 has A, which is also in the character set of S2, so S2 will take the label A. Up next S3, has {A,C} and its parent has been labelled A, so it will be labelled as A.

Parsimony Cost = 2.

Using this algorithm, we may find multiple optimal solutions. Also, Fitch's algorithm assumes that all the transition cost are same, which may not be the real world scenario. To cater this, Sankoff & Cedergren gave a dynamic programming [algorithm](https://swetakum.github.io/Sankoff's-Algortihm/).
