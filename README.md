# 스팸 메일 분류기

인공지능 수업(2021년 1학기, 인천대) 중간고사 과제. *Hands-On Machine Learning* 3장 연습문제 3-4 **Spam classifier**를 구현했다.

담당: 유용석 교수님

---

## 내용

| 노트북 | 문제 |
|---|---|
| `중간고사1_Spam_Filter.ipynb` | 스팸/햄 메일 분류기 구현 |
| `중간고사2_한승준.ipynb` | 중간고사 2번 문제 |

---

## 스팸 분류기

**데이터** — [Apache SpamAssassin 공개 코퍼스](http://spamassassin.apache.org/old/publiccorpus/)의 `easy_ham`과 `spam` 세트를 내려받아 사용한다.

**흐름**

1. 코퍼스 다운로드 및 압축 해제
2. 원본 이메일 파싱 (헤더 / 본문 / MIME 구조)
3. 본문을 분류에 쓸 수 있는 형태로 변환
4. scikit-learn 분류기 학습 및 평가

`sklearn ≥ 0.20`, `Python ≥ 3.5`이 필요하다.

---

## 실행

Colab에서 바로 열 수 있다 — 각 노트북 상단의 **Open in Colab** 배지를 누르면 된다.

로컬 실행:

```bash
pip install scikit-learn numpy matplotlib
jupyter notebook 중간고사1_Spam_Filter.ipynb
```

데이터는 노트북이 실행 시점에 자동으로 내려받는다.
