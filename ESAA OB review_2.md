# ESAA OB 수상작 리뷰 (2)

### [ 2024 NH 투자증권 빅데이터 경진대회 ****]

데이터

1. **NH_CONTEST_NW_FC_STK_IEM_IFO.csv [파일]**
- 설명: 8월 27일 기준 해외종목 정보.
- 컬럼 정보:
- TCK_IEM_CD: 티커종목코드
- FC_SEC_KRL_NM: 외화증권한글명
- FC_SEC_ENG_NM: 외화증권영문명
- STK_ETF_DIT_CD: 주식/ETF구분코드
- LTG_TOT_STK_QTY: 상장주식총수량
- FC_MKT_DIT_CD: 외화시장구분코드
- CO_ADR: 회사주소
- WEB_ADR: 웹주소
- BTP_CFC_NM: 업종분류명
- CEO_NM: CEO명
- ENG_UTK_OTL_CTS: 영문사업개요내용
- SER_CFC_NM: 섹터분류명
- IDS_NM: 산업명
- MKT_PR_TOT_AMT: 시가총액

1. **NH_CONTEST_STK_DT_QUT.csv [파일]**
- 설명: 2024년 05월 28일부터 2024년 08월 27일까지 NH_CONTEST_NW_FC_STK_IEM_IFO.csv에 있는 종목 일자별 시세 정보
- 컬럼 정보:
- BSE_DT: 거래일자
- TCK_IEM_CD: 티커종목코드
- IEM_ONG_PR: 종목시가
- IEM_HI_PR: 종목고가
- IEM_LOW_PR: 종목저가
- IEM_END_PR: 종목종가
- BF_DD_CMP_IND_PR: 전일대비증감가격
- BF_DD_CMP_IND_RT: 전일대비증감율
- ACL_TRD_QTY: 누적거래수량
- TRD_CST: 거래대금
- SLL_CNS_SUM_QTY: 매도체결합계수량
- BYN_CNS_SUM_QTY: 매수체결합계수량
- SBY_BSE_XCG_RT: 환율

1. **NH_CONTEST_NHDATA_STK_DD_IFO.csv [파일]**
- 설명: 2024년 05월 28일부터 2024년 08월 27일까지 NH데이터 기반 주식 일별 정보.
- 컬럼 정보:
- BSE_DT: BSE_DT
- TCK_IEM_CD: 티커종목코드
- TOT_HLD_ACT_CNT: 총보유계좌수
- TOT_HLD_QTY: 총보유수량
- TCO_AVG_HLD_QTY: 당사평균보유수량
- TCO_AVG_HLD_WHT_RT: 당사평균보유비중비율
- TCO_AVG_EAL_PLS: 당사평균평가손익
- TCO_AVG_PHS_UIT_PR: 당사평균매입단가
- TCO_AVG_PFT_RT: 당사평균수익율
- TCO_AVG_HLD_TE_DD_CNT: 당사평균보유기간일수
- DIST_HNK_PCT10_NMV: 분포상위10퍼센트수치
- DIST_HNK_PCT30_NMV: 분포상위30퍼센트수치
- DIST_HNK_PCT50_NMV: 분포상위50퍼센트수치
- DIST_HNK_PCT70_NMV: 분포상위70퍼센트수치
- DIST_HNK_PCT90_NMV: 분포상위90퍼센트수치
- BSE_END_PR: 기준종가
- LSS_IVO_RT: 손실투자자비율
- PFT_IVO_RT: 수익투자자비율
- IFW_ACT_CNT: 신규매수계좌수
- OFW_ACT_CNT: 전량매도계좌수
- VW_TGT_CNT: 종목조회건수
- RGS_TGT_CNT: 관심종목등록건수

1. **NH_CONTEST_NHDATA_IFW_OFW_IFO.csv [파일]**
- 설명: 2024년 05월 28일부터 2024년 08월 27일까지 유입/유출 종목 데이터
- 해외종목의 유입/유출으로 한정, 최대 TOP5까지 제공
- 컬럼 정보:
- BSE_DT: 기준일자
- TCK_IEM_CD: 티커종목코드
- IFW_OFW_DIT_CD: 유입/유출구분코드
- IFW_OFW_TCK_CD: 유입/유출티커코드
- IFW_OFW_AMT_WHT_RT: 유입/유출금액비중
- IFW_OFW_RNK: 유입/유출랭크

1. **NH_CONTEST_NHDATA_CUS_TP_IFO.csv [파일]**
- 설명: 2024년 05월 28일부터 2024년 08월 27일까지 NH데이터 기반 고객 보유 정보.
- 컬럼 정보:
- BSE_DT: 기준일자
- TCK_IEM_CD: 티커종목코드
- CUS_CGR_LLF_CD: 고객구성대분류코드
- CUS_CGR_MLF_CD: 고객구성중분류코드
- CUS_CGR_ACT_CNT_RT: 고객구성계좌수비율
- CUS_CGR_IVS_RT: 고객구성투자비율

1. **NH_CONTEST_DATA_ETF_HOLDINGS.csv [파일]**
- 설명: 2024년 8월 27일 기준 ETF의 구성 종목.
- 컬럼 정보:
- ETF_TCK_CD: 대상 ETF 티커
- TCK_IEM_CD: ETF 개별 구성 종목 티커
- MKT_VLU: 보유 종목의 가치 (USD)
- FC_SEC_ENG_NM: 보유 종목의 영문명
- FC_SEC_KRL_NM: 보유 종목의 한글명
- STK_QTY: 보유 종목의 주수 (주)
- WHT_PCT: 보유 종목의 비중 (%)
- SEC_TP: 보유 종목의 타입 (ST: 주식, EF: ETF, EN: ETN, SSEF: Single-Stock ETF)

1. **NH_CONTEST_DATA_HISTORICAL_DIVIDEND.csv [파일]**
- 설명: 2022년 8월 27일부터 2024년 8월 27일까지 ETF 배당 내역.
- 컬럼 정보:
- ETF_TCK_CD: 대상 ETF 티커
- EDIV_DT: 배당락일 (YYYYMMDD)
- DDN_AMT: 배당금
- AED_STKP_DDN_AMT: 수정 배당금
- DDN_BSE_DT: 배당 기준일 (YYYYMMDD)
- DDN_PYM_DT: 지급일 (YYYYMMDD)
- PBA_DT: 공시일 (YYYYMMDD)
- DDN_PYM_FCY_CD: 배당 주기 (Quarterly: 분기배당, Weekly: 주배당, Monthly: 월배당, SemiAnnual: 반기배당, Annual: 연배당, Other: 알 수 없음)

1. **NH_CONTEST_ETF_SOR_IFO.csv [파일]**
- 설명: 2024년 05월 28일부터 2024년 08월 27일까지 ETF 점수 정보.
- 컬럼 정보:
- BSE_DT: 거래일자
- ETF_TCK_CD: 대상 ETF 티커
- MM1_TOT_PFT_RT: 1개월총수익율
- MM3_TOT_PFT_RT: 3개월총수익율
- YR1_TOT_PFT_RT: 1년총수익율
- ETF_SOR: ETF점수
- ETF_Z_SOR: ETFZ점수
- Z_SOR_RNK: Z점수순위
- ACL_PFT_RT_Z_SOR: 누적수익율Z점수
- IFO_RT_Z_SOR: 정보비율Z점수
- SHPR_Z_SOR: 샤프지수Z점수
- CRR_Z_SOR: 상관관계Z점수
- TRK_ERR_Z_SOR: 트래킹에러Z점수
- MXDD_Z_SOR: 최대낙폭Z점수
- VTY_Z_SOR: 변동성Z점수

코드 흐름

1. 데이터로 etf 점수 매기기
- 필수 라이브러리 및 데이터 불러오기
- 시가 - 종가 간 차이와 고가-저가 간 차이 사이의 괴리 파악
- 시가배당률 계산 (배당금의 평균치를 가장 최근의 종가로 나눠서 시가배당률 계산)
- 월배당, 분기배당, 반기배당 모두 연배당으로 환산

등

.

.

1. 크롤링
- 뉴스 크롤링 함수

```jsx
def crawl_news_for_ticker(ticker):
  url = f"https://~/quote/{ticker}/news/"
  print(f"Loading news for {ticker} from {url}")
  try:
    driver.get(url)
  except Exception as e:
    print(f"Error loading URL for {ticker}: {e}")
    return False
```

- 뉴스 항목, 제목, 기사 링크, 기사 본문 및 작성일 크롤링
- 7가지 기준에 대해 MinMax처리 후 점수 합산하기 위해 데이터 병함
1. 주가 예측
- Word2Vec을 사용한 뉴스기사 벡터화

```jsx
import pandas as pd
from gensim.models import Word2Vec
import numpy as np

df2['Title']=df2['Title'].fillna(")

# Title을 공백으로 분리하여 단어 리스트로 변환
sentences=[title.split() for title in df2['Title']]

# Word2Vec 모델 학습
model = Word2Vec(sentences, vector_size=100, window=5, min_count=1,workers=4)

# 각 Title에 대한 벡터 생성
def get_vector(title):
  if title =="":
    return np.zeros(100)
  vector=np.zeros(100)
  words=title.split()
  for word in words:
    if word in words:
       vector += model.wv[word]
  return vector / len(words) of words else vector
  
# 벡터 생성하여 새로운 데이터프레임에 추가
df_vectors = pd.DataFrame(df2['Title'].apply(get_vector).tolist(),columns=[f'vector_{i+1}' for i in range(100)])

result_df = pd.concat([df2, df_vectors], axis=1)
```

1. GAN_ai 학습
2. 원본 데이터와 Gan_ai를 통해 생성된 노이즈 데이터 합쳐 bagging 성능 평가.

새롭게 알게 된 내용 / 어려운 점 / 배울 점

#### 새롭게 알게 된 내용

- 뉴스 데이터를 크롤링하고 **Word2Vec을 활용해 텍스트를 벡터화하여 주가 예측에 활용**할 수 있다는 점이 새로웠다. 단어를 숫자 벡터로 변환하는 Word2Vec 방법에 대해 배웠었는데, 이를 실제로 어떻게 활용하는지 알 수 있어 유익했다.

#### 어려운 점

- GAN으로 생성한 데이터를 원본 데이터와 결합해 성능을 평가하는 과정이 다소 복잡하게 느껴졌다.

#### 배울 점

- 크롤링 기법에 대해 새롭게 배웠다. 크롤링은 인터넷 웹사이트를 돌아다니면서 필요한 데이터를 자동으로 수집하는 것을 의미하는데, 웹사이트 속 원하는 정보를 찾아내서 데이터로 저장할 수 있다는 것이 신기하고 새로웠다.