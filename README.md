# JaccardSimilarity

# 자카드 유사도 (Jaccard Similarity)

자카드 유사도(Jaccard Similarity)는 두 집합 간의 유사도를 측정하는 방법 중 하나입니다. 이는 두 집합의 교집합 크기를 합집합 크기로 나누어 계산합니다. 수식으로 표현하면 다음과 같습니다.

$$
J(A, B) = \frac{|A \cap B|}{|A \cup B|}
$$

여기서,
- \( A \)와 \( B \)는 비교하고자 하는 두 집합입니다.
- \( |A \cap B| \)는 두 집합의 교집합의 크기입니다.
- \( |A \cup B| \)는 두 집합의 합집합의 크기입니다.

## 예제

두 집합 \( A \)와 \( B \)가 다음과 같다고 가정해봅시다:
- \( A = \{1, 2, 3\} \)
- \( B = \{2, 3, 4, 5\} \)

이 경우, 교집합과 합집합은 다음과 같이 계산됩니다:
- \( A \cap B = \{2, 3\} \)
- \( A \cup B = \{1, 2, 3, 4, 5\} \)

따라서 자카드 유사도는 다음과 같습니다:
$$
J(A, B) = \frac{|A \cap B|}{|A \cup B|} = \frac{2}{5} = 0.4
$$

자카드 유사도는 0에서 1 사이의 값을 가지며, 1은 두 집합이 동일함을 의미하고 0은 두 집합이 공통 요소가 없음을 의미합니다.


# TF-IDF

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
