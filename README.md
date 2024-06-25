# huggingface tokenizer
Hugging Face Tokenizers 오픈소스 라이브러리는 텍스트 생성, 요약, 번역 등과 같은 작업에 사용되는 인기 있는 변환기 모델의 토크나이저에 대한 액세스를 제공합니다.
![rnn](https://github.com/jkm2000korea/tensorflow-nlp-tutorial-review/assets/77305773/5e68e577-a511-46fd-8e91-539681012401){: width="150%"}

1) BERT의 WordPiece 토크나이저
2) GPT-2의 바이트 수준 BPE 토크나이저
3) T5의 SentencePiece 토크나이저
4) 그리고 다른 많은 변환기의 토크나이저
   
![image](https://github.com/jkm2000korea/tensorflow-nlp-tutorial-review/assets/77305773/1858002f-6bde-4732-b62c-90b09f0d7548)



# Word to Vector(Word2Vec)
1) 거대한 텍스트 코퍼스를 가져옵니다.
2) 한 번에 한 단어씩 이동하면서 슬라이딩 창으로 텍스트를 살펴봅니다.각 단계에는 중심 단어와 문맥 단어(창 크기 이내 다른 단어)가 있습니다.
3) 중심 단어의 경우, 문맥 단어의 확률을 계산합니다.
4) 이러한 확률을 높이려면 벡터를 조정합니다.
   
![image](https://github.com/jkm2000korea/tensorflow-nlp-tutorial-review/assets/77305773/4e9870c4-0df0-409e-9e27-e1db37f1ca6a)


# # Leaky ReLU 함수
 np.maximum(a*x, x) 에서 a = 0.1 ~ 1.0

 ![image](https://github.com/jkm2000korea/tensorflow-nlp-tutorial-review/assets/77305773/26442550-be2d-4ed8-ac3f-ca21f25b840c)



# 소프트 맥스(SOFTMAX)

- Softmax(소프트맥스)는 입력받은 값을 출력으로 0~1사이의 값으로 모두 정규화
- 출력 값들의 총합은 항상 1이 되는 특성을 가진 함수
- 분류하고 싶은 클래수의 수 만큼 출력으로 구성
- 가장 큰 출력 값을 부여받은 클래스가 확률이 가장 높은 것으로 이용
  
![image](https://github.com/jkm2000korea/tensorflow-nlp-tutorial-review/assets/77305773/bd283a3b-c214-4114-b36b-20baaac980bc)
(https://miro.medium.com/v2/resize:fit:1400/0*J8gIAZofl6MlfLUK.jpeg)



# 자카드 유사도 (Jaccard Similarity)

자카드 유사도(Jaccard Similarity)는 두 집합 간의 유사도를 측정하는 방법 중 하나입니다. 이는 두 집합의 교집합 크기를 합집합 크기로 나누어 계산합니다. 수식으로 표현하면 다음과 같습니다.

$$
J(A, B) = \frac{|A \cap B|}{|A \cup B|}
$$

여기서,
- \( A \)와 \( B \)는 비교하고자 하는 두 집합입니다.
- \( |A \cap B| \)는 두 집합의 교집합의 크기입니다.
- \( |A \cup B| \)는 두 집합의 합집합의 크기입니다.

![image](https://github.com/jkm2000korea/tensorflow-nlp-tutorial-review/assets/77305773/04df3892-0e4c-4a99-8087-2067f942485c)


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
