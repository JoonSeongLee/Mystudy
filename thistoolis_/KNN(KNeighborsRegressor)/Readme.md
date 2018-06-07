
# KNeighborsClassifier()

class sklearn.neighbors.`KNeighborsClassifier`(n_neighbors=5, weights=’uniform’, algorithm=’auto’, leaf_size=30, p=2, metric=’minkowski’, metric_params=None, n_jobs=1, **kwargs)

### Parameters:	

n_neighbors : int, optional (default = 5)

    Number of neighbors to use by default for kneighbors queries.
    (근접 이웃 수 설명)

weights : str or callable, optional (default = ‘uniform’)

    weight function used in prediction. Possible values:
    (예측에 사용된 가중치 함수)
    
    ‘uniform’  : uniform weights. All points in each neighborhood are weighted equally.
                 (균일한 가중치, 각 이웃에있는 모든 점에 동일한 가중치가 적용)
                 
    ‘distance’ : weight points by the inverse of their distance. in this case, closer neighbors of a 
                 query point will have a greater influence than neighbors which are further away.
                 (거리의 역수로 가중치, 이 경우 포인트의 인접한 이웃들이 멀리 떨어져있는 이웃들보다 더 큰 영향을 미침)
                 
algorithm  : {‘auto’, ‘ball_tree’, ‘kd_tree’, ‘brute’}, optional

    Algorithm used to compute the nearest neighbors:
    (가장 가까운 이웃을 계산하는 데 사용되는 알고리즘)
    
    ‘ball_tree’ will use BallTree
    ‘kd_tree’ will use KDTree
    ‘brute’ will use a brute-force search.
    ‘auto’ will attempt to decide the most appropriate algorithm based on the values passed to fit method.
    Note: fitting on sparse input will override the setting of this parameter, using brute force.

leaf_size : int, optional (default = 30)

    Leaf size passed to BallTree or KDTree. This can affect the speed of the construction and query, 
    as well as the memory required to store the tree. The optimal value depends on the nature of the problem.
    (BallTree 또는 KDTree에 전달 된 리프 크기)
    
p : integer, optional (default = 2)

    Power parameter for the Minkowski metric. When p = 1, this is equivalent to using manhattan_distance (l1),
    and euclidean_distance (l2) for p = 2. For arbitrary p, minkowski_distance (l_p) is used.

metric : string or callable, default ‘minkowski’

    the distance metric to use for the tree. The default metric is minkowski, and with p=2 is equivalent to 
    the standard Euclidean metric. See the documentation of the DistanceMetric class for a list of available metrics.

metric_params : dict, optional (default = None)

    Additional keyword arguments for the metric function.

n_jobs : int, optional (default = 1)

    The number of parallel jobs to run for neighbors search. If -1, then the number of jobs is set to 
    the number of CPU cores. Doesn’t affect fit method.
    (인접 항목 검색을 위해 실행할 병렬 작업 수입니다. -1이면 작업 수는 CPU 코어 수로 설정됩니다)

| Methods                                       |                                                               |
|-----------------------------------------------|---------------------------------------------------------------|
| fit(X, y)                                     | X를 학습 데이터로, y를 목표 값 |
| get_params([deep])                            | Get parameters for this estimator.                            |
| kneighbors([X, n_neighbors, return_distance]) | 한 지점의 K- 이웃을 찾습니다.                            |
| kneighbors_graph([X, n_neighbors, mode])      | X의 점에 대한 k- 이웃의 (가중치가있는) 그래프를 계산합니다.  |
| predict(X)                                    | 제공된 데이터의 클래스 레이블을 예측합니다.                |
| predict_proba(X)                              | 테스트 데이터 X에 대한 확률 추정치.             |
| score(X, y[, sample_weight])                  | 주어진 테스트 데이터 및 레이블의 평균 정확도를 반환합니다.  |
| set_params(**params)                          | 이 estimator 매개 변수를 설정.                       |
