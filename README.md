# 스팸 메일 분류기

*Hands-On Machine Learning* 3장 연습문제 3-4 **Spam classifier** 구현. 인공지능 수업(2021년 1학기, 인천대 유용석 교수님) 과제로 작성했다.

---

## 데이터

[Apache SpamAssassin 공개 코퍼스](http://spamassassin.apache.org/old/publiccorpus/)의 `easy_ham`(정상 메일)과 `spam` 세트를 내려받아 사용한다. 노트북이 실행 시점에 자동으로 받으므로 별도 준비가 필요 없다.

## 흐름

1. 코퍼스 다운로드 및 압축 해제
2. 원본 이메일 파싱 — 헤더 / 본문 / MIME 멀티파트 구조 처리
3. 본문을 분류에 쓸 수 있는 특징으로 변환
4. scikit-learn 분류기 학습 및 평가

---

## 실행

상단의 **Open in Colab** 배지로 바로 열 수 있다. 로컬 실행:

```bash
pip install scikit-learn numpy matplotlib
jupyter notebook spam_filter.ipynb
```

`Python ≥ 3.5`, `scikit-learn ≥ 0.20`이 필요하다.
