<div align=center>
  
![header](https://capsule-render.vercel.app/api?type=rounded&color=36FADE&fontColor=F5F884&height=130&section=header&text=%20purchase-recommend-system%20&animation=scaleIn&fontSize=40&fontAlign=50&fontAlignY=50)

</div>
<br>

## :clipboard: 구매 연계 추천 시스템 :computer:

<br>

### 목차

```
1. 서비스 소개
2. 유사 서비스
3. 오픈소스 목록
4. 오픈소스 특징 및 
5. 오픈소스 API 및 라이선스
6. DFD(data flow diagram)
7. 실행화면
```

<br>

#### :recycle: 서비스 소개

```
  구매 연계 추천 서비스는 사용자가 웹사이트에 접속한 후 및 상품을 구매하면 사용자와 관련 있는 상품들을 추천하는 
서비스이다.
  이 추천 서비스를 적용하면 고객들의 구매 서비스 만족도를 향상시킬 수 있을 뿐만 아니라 지속적인 웹사이트 이용을 유도
하여 상품 구매량 증가 및 기존 고객층 유지와 신규 고객 가입을 이끌어 최종적으로 수익이 증가하는 효과를 얻을 수 있다.
  추천 서비스는 회원제로 운영된다. 사용자는 우선 웹사이트에 접속한다. 웹사이트에 접속하면 구매 이력을 조회한 결과를 
이용하여 서비스를 제공받을 수 있다. 또한 원하는 물건을 검색하여 구매를 완료하면 구매 이력 및 물건과 관련 있는 기타 
물건들의 정보를 조합하여 사용자에게 맞춰진 물품들을 추천한다.
  서비스는 추천 시 여러 가지 추천 알고리즘들이 이용되어 높은 정확성을 지닌 채 상품을 추천할 수 있다.
```

<br>

#### :mag_right: 유사 서비스

```
1. 쿠팡
* 유사점
  - 홈페이지 초기 화면부터 상품 추천
  - 검색시 분류기준으로 나열하여 상품 확인 가능
  - 상품 상세 페이지로 추가적으로 추천
* 차이점
  - 홈페이지 초기 화면에서 쿠팡은 특가 이벤트, 기간 이벤트로 추천하지만 본 서비스는 사용자 정보를 기반으로 추천
  - 상품 상세 페이지에서 쿠팡은 쿠팡내의 상품을 추천해주지만 본 서비스는 다른 웹 사이트의 광고를 띄움

2. 네이버
* 유사점
  - 홈 화면에서의 광고창
  - 검색어 입력시 검색어와 관련된 네이버 쇼핑 안의 상품과 외부 광고 사이트의 링크
* 차이점
  - 홈 화면에서의 광고창이 네이버는 무작위 광고지만 본 서비스에서는 사용자 정보 기반 광고
```

<br>

#### :school_satchel: 오픈소스 목록

```
1. JQuery Validation
2. WordPress
3. SOLR
4. Coupang Category Recommendation API
5. React
6. OpenRefine
7. Apache Spark
8. Scrapy
9. Tensorflow
10. Tensorflow Serving
```

<br>

#### :school_satchel: 오픈소스 특징 및 역할

* Coupang Category Recommendation API
```
- 가지고 있는 상품정보(상품명, 브랜드, 속성 등)을 입력하면 해당 정보와 가장 일치하는 카테고리를 찾아서 제안해주는 서비스이다.
- 과거 등록되었던 상품의 쿠팡 카테고리를 시스템에 학습시킨 머신러닝 모델로 서비스되고 있다.
- 부정확한 정보 입력 시 정확한 카테고리가 추천되지 않을 수 있다.
```

```
사용자가 가지고 있는 제품의 데이터(사용자 프로필 데이터)로 사용자 기반 추천을 하여 추천된 카테고리 정보를 생성
```
* Tensorflow
```
- 2015년 구글에서 공개
- 주로 Python 언어를 통해 작동됨
- 데이터가 주어졌을 때 스스로 학습하는 머신러닝 구현
- Learning to rank 알고리즘 등 다양한 알고리즘을 지원하여 그에 맞게 학습 가능
- Tensor라는 데이터 형식을 이용하여 연산 진행
- 시각화 도구인 Tensorboard를 지원하여 학습과정 추적 가능
- 지속적인 성능 개선과 수정을 통한 빠르고 안정적인 성능 지원
```

```
Tensorflow에 구현된 알고리즘 중 Learing to rank 알고리즘을 사용하여 추천 데이터들의 우선순위를 기록한 데이터 생성
```

* Tensorflow Serving
```
- Tensorflow 데이터 배포를 위해 개발
- Tensorflow 데이터에 대한 버전 관리 지원
- Tensorflow 데이터의 크기가 큰 경우 여러 개로 나누어 배포
- REST API를 지원하여 사용자에게 데이터 전달 가능
```

```
Tensorflow를 이용하여 만들어진 데이터를 사용자에게 전달하기 위해 사용됨
```

<br>

#### :school_satchel: 오픈소스 API 및 라이선스

| open source           | input data | output data | API         |  license |
| ------------------ | ---------- | ----------- | ----------- | ----------- |
| tensorflow         | files      | tensor      | tf.data API | Apache 2.0 |
| tensorflow serving | tensor     | json        | Tensorflow Serving API | Apache 2.0 |
| Coupang Open API | json | json | Category Recommendation API | MIT License

<br>

#### :arrows_counterclockwise: 자료흐름도 (Data Flow Diagrams)

<div align=center>
  
![image](./dfd%20picture.PNG)

</div>
