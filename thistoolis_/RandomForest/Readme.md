

# RandomForestClassifier()

class sklearn.ensemble.`RandomForestClassifier`(n_estimators=10, criterion=’gini’, max_depth=None, min_samples_split=2, min_samples_leaf=1, min_weight_fraction_leaf=0.0, max_features=’auto’, max_leaf_nodes=None, min_impurity_decrease=0.0, min_impurity_split=None, bootstrap=True, oob_score=False, n_jobs=1, random_state=None, verbose=0, warm_start=False, class_weight=None)



### Parameters:	

n_estimators : integer, optional (default=10)

    결정트리의 갯수


criterion : string, optional (default=”gini”)

    The function to measure the quality of a split. Supported criteria are “gini” for the Gini impurity and “entropy” for the information gain. Note: this parameter is tree-specific.
    

max_features : int, float, string or None, optional (default=”auto”)

    고려해야 할 feature의 수 :
    
    int   :  then consider max_features features at each split.
    float :  백분율
    auto  :  sqrt(n_features)
    sqrt  :  sqrt(n_features) 
    log2  :  log2(n_features)
    None  :   n_features.
    

max_depth : integer or None, optional (default=None)

    나무의 최대 깊이
    (모든 잎이 순수하거나 모든 잎이 min_samples_split 샘플보다 작아 질 때까지 노드가 확장됩니다.)
    

min_samples_split : int, float, optional (default=2)

    분할하는데 필요한 최소 샘플 수
    

min_samples_leaf : int, float, optional (default=1)

    리프에 있어야 하는 최소 샘플 수


min_weight_fraction_leaf : float, optional (default=0.)

    리프에 있어야 하는 총 가중치 중 최소 가중치. sample_weight가 제공되지 않은 경우 샘플의 가중치는 동일합니다.


max_leaf_nodes : int or None, optional (default=None)

    max_leaf_nodes가 있는 나무를 최상의 방법으로 성장시킵니다. 최상의 노드는 불순물의 상대적 감소로 정의됩니다.
    
    None이면 리프의 개수에 제한이 없습니다.


bootstrap : boolean, optional (default=True)

    부트스트랩 샘플을 사용할지 여부
    

oob_score : bool (default=False)

    Whether to use out-of-bag samples to estimate the generalization accuracy.

n_jobs : integer, optional (default=1)

    병렬로 실행할 작업 수입니다. -1이면 작업 수는 코어 수로 설정됩니다.
    

### Methods
| Methods                                       |                                                               |
|-----------------------------------------------|---------------------------------------------------------------|
| apply(X)                                      | 포리스트의 트리를 X에 적용하고 리프 인덱스를 반환합니다.                   |
| decision_path(X)                              | 포리스트의 결정 경로를 반환합니다.                                    |
| fit(X, y[, sample_weight])                    | 훈련 세트 (X, Y)에서 forest of trees을 건설합니다.                |
| get_params([deep])                            | 이 견적서의 매개 변수를 가져옵니다.  |
| predict(X)                                    | X에 대한 클래스를 예측합니다.                |
| predict_log_proba(X)                          | X에 대한 클래스 로그 확률 예측합니다.             |
| predict_proba(X)                              | X에 대한 클래스 확률을 예측합니다.  |
| score(X, y[, sample_weight])                  | 주어진 테스트 데이터 및 레이블의 평균 정확도를 반환합니다.               |
| set_params(**params)                          | estimator의 매개 변수를 설정하십시오.                       |

