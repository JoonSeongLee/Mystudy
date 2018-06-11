
# KNeighborsClassifier()


class sklearn.cluster.`KMeans`(n_clusters=8, init=’k-means++’, n_init=10, max_iter=300, tol=0.0001, precompute_distances=’auto’, verbose=0, random_state=None, copy_x=True, n_jobs=1, algorithm=’auto’)

### Parameters:	

n_clusters : int, optional, default: 8

    형성 할 클러스터 수 및 생성 할 중심 수입니다.


max_iter : int, default: 300

    단일 실행에 대한 k- 평균 알고리즘의 최대 반복 횟수

tol : float, default: 1e-4

    수렴에 대한 관성에 대한 상대 허용 오차
    

n_jobs : int

    계산에 사용할 작업 수. 이는 각각의 n_init 실행을 병렬로 계산하여 작동합니다.

   
algorithm : “auto”, “full” or “elkan”, default=”auto”

### Attributes
.cluster_centers_ : array, [n_clusters, n_features]

    클러스터 센터의 좌표

.labels_ : 

    각 점의 라벨

.inertia_ : float

    가장 가까운 클러스터 센터에 대한 샘플의 제곱거리의 합.

| Methods                                       |                                                               |
|-----------------------------------------------|---------------------------------------------------------------|
| fit(X[, y])                                   | k-means 클러스터링을 계산합니다. |
| get_params([deep])                            | Get parameters for this estimator.                            |
| fit_predict(X[, y]) | 클러스터 센터를 계산하고 각 샘플에 대한 클러스터 인덱스를 예측합니다.                   |
| fit_transform(X[, y])	     | 클러스터링을 계산하고 X를 클러스터 거리 공간으로 변환합니다.  |
| predict(X)                                    | 제공된 데이터의 클래스 레이블을 예측합니다.                |
| predict_proba(X)                              | X가 속한 각 샘플에 가장 가까운 클러스터를 예측합니다.             |
| score(X[, y])                  | Opposite of the value of X on the K-means objective. |
| set_params(**params)                          | 이 estimator 매개 변수를 설정.|
| transform(X)                          | 이 estimator 매개 변수를 설정.                       |


[link](http://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html)

