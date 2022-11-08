# 이태원 압사 사고 예측 가능했나?
## 이태원에서 압사사고 일어난적이 없는데, 어떻게 예측이 가능했다고 말하는걸까?
- 데이터를 통해서 살펴본 압사사고의 가능성
- DATA
-   - 2017~2021 일별 시간별 지하철 승하차 데이터
-   - 2017~2021 일별 시간별 유동인구 데이터
-   - 2021 기준 서울시 상권데이터
- Progress
-   - 평균 인원보다 피크치를 보는것이 유의미하다고 생각
-   - (data.max()-data.mean())/data.std()를 확인하여 살펴보는 것으로 문제를 풀어나가자
-   - 상권데이터의 경우 folium에 날려서 상권의 집적도를 확인하자 
-   - -> 이것은 인구가 분산되기 힘든지를 확인하는 척도가 될 수 있을것 같다.

### 상권 scatter
<img width="1088" alt="Screen Shot 2022-11-09 at 8 49 13" src="https://user-images.githubusercontent.com/112222918/200701307-c76f6362-1f24-46bc-a308-b13a9a937485.png">

### 상권 barplot
<img width="1283" alt="Screen Shot 2022-11-09 at 8 49 40" src="https://user-images.githubusercontent.com/112222918/200701567-f3bd1f33-ce6a-4147-af98-579e948bed30.png">

### 유동인구 barplot
<img width="1152" alt="Screen Shot 2022-11-09 at 8 50 06" src="https://user-images.githubusercontent.com/112222918/200701645-7ccff554-1076-40c4-aba5-c0efb0294dc7.png">

### 지하철 barplot
<img width="1242" alt="Screen Shot 2022-11-09 at 8 51 04" src="https://user-images.githubusercontent.com/112222918/200701688-9b39b951-409f-47e2-b34d-a3dda421806d.png">


```
.
├── README.md
├── final_.ipynb
├── preprocessing_metro
│   ├── Metro_2017_2021.jpg
│   ├── metro_diff.ipynb
│   ├── preprocess_metro_1.ipynb
│   └── preprocess_metro_2.ipynb
├── preprocessing_population
│   ├── population_diff_1.ipynb
│   └── population_diff_2.ipynb
├── preprocessing_pub
│   ├── pub_barchart.ipynb
│   └── pub_folium.ipynb
└── raw_data
    ├── seoul_bus_raw
    ├── seoul_metro_raw
    ├── seoul_population_raw
    ├── seoul_pub
    └── seoul_road_raw

9 directories, 10 files

```
