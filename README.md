TF-IDF Example
In order to fully understand how TF-IDF works, I will give you a concrete example. Let's assume that we have a collection of four documents as follows:

𝑑
1
d 
1
​
 : "The sky is blue.

𝑑
2
d 
2
​
 : "The sun is bright today."

𝑑
3
d 
3
​
 : "The sun in the sky is bright."

𝑑
4
d 
4
​
 : "We can see the shining sun, the bright sun."

Task: Determine the tf-idf scores for each term in each document.

Step1: Filter out the stopwords. After removing the stopwords, we have

𝑑
1
d 
1
​
 : "sky blue

𝑑
2
d 
2
​
 : "sun bright today"

𝑑
3
d 
3
​
 : "sun sky bright"

𝑑
4
d 
4
​
 : "can see shining sun bright sun"

Step2: Compute TF, therefore, we find document-word matrix and then normalize the rows to sum to 1.

![image](https://github.com/jkm2000korea/tensorflow-nlp-tutorial-review/assets/77305773/8e993bd2-4614-490e-894a-a0d79ce73e7e)

![image](https://github.com/jkm2000korea/tensorflow-nlp-tutorial-review/assets/77305773/13f84278-fdcc-4219-ab3f-76cbc1f9cb83)
