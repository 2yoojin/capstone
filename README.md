![header](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=350&section=header&text=Capstone&nbsp;&nbsp;Design&stroke=3A2F32&strokeWidth=2&animation=twinkling)

Team Member
-----------------

<table>
  <tr>
    <th align="center"><a href="https://github.com/SeokjunShin"><img src="https://avatars.githubusercontent.com/u/149030300?v=4" width="150x;" alt=""/><br /></a></th>
    <th align="center"><a href="https://github.com/wnstndks"><img src="https://avatars.githubusercontent.com/u/125172335?v=4" width="150x;" alt=""/><br /></a></th>
        <th align="center"><a href="https://github.com/lcm1120"><img src="https://avatars.githubusercontent.com/u/104052426?v=4" width="150x;" alt=""/><br /></a></th>
    <th align="center"><a href="https://github.com/2yoojin"><img src="https://avatars.githubusercontent.com/u/113568993?v=4" width="150x;" alt=""/><br /></a></th>
  </tr>
  <tr>  
    <th><a href="https://github.com/SeokjunShin"><b>신석준</b></a></th>
    <th><a href="https://github.com/wnstndks"><b>안준수</b></a></th>
    <th><a href="https://github.com/lcm1120"><b>임채민</b></a></th>
    <th><a href="https://github.com/2yoojin"><b>이유진</b></a></th>
  </tr>
</table>

<br/>

Contents
-----------------
> [프로젝트 개요](#프로젝트-개요)
>
> [배경 지식](#배경지식)
> 
> [프로젝트 목표](#프로젝트-목표)
>
> [베이스라인 모델](#베이스라인-모델)
>
> [참조 사이트](#참조-사이트)

<br/>

프로젝트 개요
-----------------
<p> [1] 일반적인 인공지능 모델은 빅데이터 학습을 통해 규칙을 찾아내고 성능을 확보한다. </p>
<p> [2] 특이한 사례 (전례없는 집중호우, 기계의 고장 등)는 많은 피해를 발생시키고 문제가 될 수 있으나, 샘플이 적어 일반적인 인공지능 모델로 다루기 어렵다. </p>
<p> [3] 이상치를 예측하거나 다룰 수 있는 방법론을 공부하고 실제 데이터에 적용하여 분석모델의 성능 향상을 증명하거나 활용성을 제시한다. </p>

<br/>

배경지식
-----------------

<h3> 이상치(Outlier)란</h3>
<p>데이터 분석에서 특정 데이터셋 내의 다른 관측값들과 크게 벗어난 데이터 포인트이다.
이상치는 여러 가지 이유로 발생할 수 있으며, 분석 과정에서 중요한 역할을 하기에, 이상치를 적절히 처리하는 것은 데이터 분석의 정확성과 신뢰성을 높이는 데 필수적이다.</p>
<img src="https://github.com/2yoojin/capstone/assets/125172335/acba6ea8-2100-4f1f-a0c8-676804db0db6"/>

<br/><br/>

프로젝트 목표
-----------------

**주제**:
한강내 대교별 수위 데이터 이상치값 예측

**수집 방법** : 
한강홍수통제소 제공 데이터 활용(한강 수위, 이상치 기준, 댐 방수량), 기상청 데이터 활용(지역별 강수량)

**측정 기간** : 
각 대교별 2010년~2023년까지의 데이터 

**측정 장소** : 
한강 내 대교별 측정

<br/>

베이스라인 모델
-----------------
<h3><a href="https://github.com/ashfarhangi/aa-forecast">AA-Forecast</a></h3>
<p> 이상 현상 자동 추출 & 확률예측을 통해 최적화하는 새로운 프레임워크</p>
<img src="https://private-user-images.githubusercontent.com/125172335/334250617-9b532b74-8fc4-4f07-87ed-6ff002cad78f.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTY4NzMyOTksIm5iZiI6MTcxNjg3Mjk5OSwicGF0aCI6Ii8xMjUxNzIzMzUvMzM0MjUwNjE3LTliNTMyYjc0LThmYzQtNGYwNy04N2VkLTZmZjAwMmNhZDc4Zi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNTI4JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDUyOFQwNTA5NTlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT00ZGU4Yjc4ZjJmNzkyMTVkMmQxMTQ1ODQ3ODUwYTA4ZWY1MDI0Y2JmMGExYjY2NTcxOWNiZjk3NjQ2MjE3NzQ5JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.qIcfUMf2aB6iTizgnke1t5MX1YR2G1B5_HxyLyVHgdQ"/>
<p> <h3>Data Preprocessing</h3> 데이터의 seasonal, trend, anomalies, residual를 분석하는 Star Decompostion</p>

```python
def AA_decompose(df, period=24, lo_frac=0.6, lo_delta=0.01, warning_level=None):
    lowess = sm.nonparametric.lowess
    water_level = np.asanyarray(df['wl']).squeeze()
    anomalies = anomaly_detection(water_level, warning_level)
    trend = lowess(water_level, [x for x in range(len(water_level))],
                   frac=lo_frac,
                   delta=lo_delta * len(water_level),
                   return_sorted=False)
    detrended = water_level / trend
    period = min(period, len(water_level))
    period_median = np.array([pd_nanmean(detrended[i::period])
                              for i in range(period)])

    seasonal = np.repeat(period_median, len(water_level) // period + 1)[:len(water_level)]
    resid_inter = detrended / seasonal
    resid_inter[0] = 1
    resid = resid_inter.copy()
    
    return trend, seasonal, anomalies, resid
```

<p> <h3>Trend / Test Set</h3> 2022년 이전의 데이터를 훈련 데이터로 사용, 2022년부터 2023년까지의 데이터 테스트 데이터로 분리하여 모델 훈련 및 평가</p>
<p> <h3>Anomaly Definition</h3> Interest 경보 수준 이상인 값들을 anomalies = True로 설정</p>
<p> <h3>Model Implementation </h3> 
<p> > Features : 한강 유량, 서울 강수량, 한강 상류 강수량, 댐 방류량.</p>
<p> > Model Model Structure : Attention 메커니즘 적용하여 이상치에 가중치 부여, 이상치 비율이 1% 내외인 관측소들만 선별하여 모델 훈련 진행</p>
<p> > Hyperparameters : Dropout = 0.5, Epochs = 200, lstmcell1 = 256, lstmcell2 = 128, dense1 = 64.</p>
</p>

```python

### DEFINE FORECASTER ###
inputs1 = Input(shape=(X_train1.shape[1], X_train1.shape[2]))
lstm1 = GRU(lstmcell1, return_sequences=True,
            dropout=dropOut)(inputs1, training=True)
lstm1 = GRU(lstmcell2, return_sequences=False,
            dropout=dropOut)(lstm1, training=True)
dense1 = Dense(dense1)(lstm1)
out1 = Dense(1)(dense1)

model1 = Model(inputs1, out1)
model1.compile(loss=lossmetric, optimizer='adam', metrics=[lossmetric, 'accuracy'])

### FIT FORECASTER ###
train_size = int(len(X_train1) * 0.8)

history = model1.fit(X_train1[:train_size], y_train1[:train_size], validation_data=(X_train1[train_size:], y_train1[train_size:]), epochs=epochs, batch_size=256, verbose=2, shuffle=False)
```

<p>
<h3>Model Evaluation</h3>
<p> > Evaluation Metrics : MSE, MAE 메인 지표, Adjusted R-Squared 서브 지표 채택</p>
<p> > Baseline Model : GRU, LightGBM, Prophet 베이스라인으로 삼아 성능 평가 진행</p>
</p>

<br/>

참조 사이트
-----------------
> <h3><a href="https://www.hrfco.go.kr/main.do">한강 홍수 통제소</a></h3>
> <h3><a href="https://apihub.kma.go.kr/">기상청 API 허브</a></h3>

<br/>

결론
-----------------

한강 홍수통제소에서 제공하는 다양한 관측소 데이터를 바탕으로 Star 분해법과 attention 메커니즘을 적용하여 *이상치* 예측의 정확성을 높였다. 
GRU, LightGBM, Prophet 모델을 베이스라인으로 삼아 성능을 비교한 결과, AA-Forecast 모델을 활용하였을 때, *이상치* 예측에서 가장 우수한 성능을 보였다. 
이러한 결과는 한강 수위를 사전에 예측함으로써 위험 상황에 대한 조기 경보와 대비책 마련에 큰 도움을 줄 수 있음을 시사한다. 
앞으로 다양한 데이터와 상황을 고려한 추가 연구를 통해 모델의 성능을 더욱 향상시킬 수 있을 것으로 기대된다.
