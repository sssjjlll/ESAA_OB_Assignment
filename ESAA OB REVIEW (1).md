# ESAA OB 수상작 리뷰 (1)

### [ **피싱·스캠 예방을 위한 서비스 개발 경진대회** ]

데이터

1. KOR_phishing - 한국어 메신저 피싱 메시지 데이터
- 규모 10,000건 +
1. KorCCVi v2.1 - 보이스피싱 통화 전사 데이터
- 5,000건 +

코드 흐름

1. 환경 설정 및 라이브러리 설치
2. 데이터 수집 및 전처리
3. AI 모델 구현

3.1 KoBERT 기반 텍스트 분류기

```jsx
MODEL_NAME = 'klue/bert-base'

try:
  tokenizer = AutoTokenizer.from_pretrained(MODEL_NAME)
  model = AutoModelForSequenceClassifiation.from_pretrained(
    MODEL_NAME,
    num_labels=2,
    problem_type="single_label_classification"
  )
  model.to(device)
  print(f"{MODEL_NAME} 모델 로드 완료")
except Exception as e:
  print(f"모델 로드 실패: {e}")
  print("베이스라인 모델로 진행합니다.")
  
```

```jsx
# Pytorch Dataset 클래스
class PhishingDataset(Dataset):
  def __init__(self, texts, labels, tokenizer, max_length=128):
    self.texts = texts
    self.labels = labels
    self.tokenizer = tokenizer
    self.max_length = max_length
  
  def __len__(self):
    return len(self.texts)
    
  def __getitem__(self,idx):
    text = str(self.texts[idx])
    label = self.lavels[idx]
    
    encoding = self.token.tokenizer(
      text,
      max_length=self.max_length,
      padding='max_length',
      truncation=True,
      return_tensors='pt'
   ) 
   
   return{
     'input_ids': encoding['input_ids'].flatten(),
     'attenttion_mask': encoding['attention_mask'].flatten()
     'labels': torch.tensor(label, dtype=torch.long)
   }
 
# 데이터 분할
X_train, X_test, y_train, y_test = train_test_split(
  df['text'].values,
  df['label'].values,
  test_size=0.2,
  random_state=42,
  stratify=df['label'].values
)

print(f"학습 데이터: {len(X_train)}개")
print(f"테스트 데이터: {len(X_test)}개")
```

3.2 URL 피싱 탐지 모델

3.3 설명 가능한 AI

1. 통합 분석 파이프라인
2. 교육 시뮬레이션 모듈
3. 성능 평가 및 시각화
4. 데모 및 테스트

새롭게 알게 된 내용 / 어려운 점 / 배울 점

#### 새롭게 알게 된 내용

- KoBERT와 같은 사전학습 언어모델을 활용하면 한국어 텍스트의 피싱 여부를 분류할 수 있다는 점을 새롭게 알게 되었다.
- 하나의 모델만 사용하는 것이 아니라 텍스트, URL 등 다양한 정보를 결합하여 피싱을 탐지할 수 있다는 점을 알게 되었다.

#### 어려운 점

- AI 모델 구현뿐만 아니라 성능 평가와 시각화, 데모까지 연결하는 전체적인 파이프라인을 이해하는 것이 어려웠다.

#### 배울 점

- 텍스트 데이터를 분석할 때 단순히 데이터를 사용하는 것이 아니라, 토큰화·패딩 등의 전처리 과정을 거쳐 모델이 이해할 수 있는 형태로 변환하는 것이 중요하다는 점을 배웠다.
- 한국어 텍스트 분류에서 KoBERT와 같은 사전학습 언어모델을 활용하면 텍스트의 특성을 효과적으로 학습할 수 있다는 점을 배웠다.