# Week 3 Summary 분산 딥러닝

## 개요
분산 딥러닝 챕터이지만 현재 책에서는 프레임워크 두개 소개 그리고 간단한 예제 소개(SparkML,H2O)

# 1.SparkML/DL
* Spark 기반 ML 
* 이제는 알만한 사람들은 다 아는 인메모리 기반 빅데이터 분석 프레임워크
* 2011년 UC Berkeley에서 개발 
* 일반적인 ML문제들에서 iteration을 거치면 거칠수록 성능적으로 하둡보다 우수한 모습을 보여 주목
* RDD( Resilient Distributed Datasets )라는 비휘발성 메모리 자료구조 모델을 이용한 방식이 특징
* 구현자체도 scala analysis용 코드 작성도 scala가 용이 이후 scala가 꽤 주목받는 계기가 됨 
* zeppelin으로 spark cluster만 설치되어 있으면 Data scientist들이 비교적 간편하게 Data Analysis가 가능

# 1.1 TensorflowOnSpark
* DL이 대두되면서 기존에 Spark나 Scala에서 점유율이 높던 CF나 MF 추천 알고리즘문제들이 state of the art 자리를 DL에게 내주게 됨( 물로 OTT는 추천으로 돈 잘 벌지만 )
* TensorFlowOnSpark는 기존의 spark 인프라를 활용해서 DL을 돌리는 것이 효율성이 높았으므로 발빠르게 릴리즈
* 그러나 후술할 TensorFlow가 애초에 분산 기능을 가지고 있기 때문에 그다지 많이 주목받거나 많이 사용되지는 않음

# 2. H2O
* java 기반 ML 프레임워크
* Distributed ,In memory ,multi language ineterpreter, AutoML 등의 특징을 가지고 있는 ML프레임워크

# 2.1 H2O AutoML
* 자동적으로 algorithm selection, feature generation, hyperparameter tuning, iterative modeling, model assessment 을 알아서 해준다. 
* 그러나 위 내용 자체가 분산환경에 대한 부분에서는 크게 연관이 없어서 더 들여다 보지는 x

# 3. TensorFlow

* google에서 나온 DL Framework 보통 DL이 뜨면서 그 알고리즘에만 주목하지만 
* https://arxiv.org/pdf/1603.04467.pdf 이 논문을 볼 필요가 있음
* 위 논문의 공동저자 중에 익숙한 이름이 있는데 "Jeffrey Dean" 이 있음 
* Jeffrey Dean - MapReduce 참여, Spanner, BigTable 등 대단한 분산 기반의 프레임워크들을 직접 진두지휘한 사람
* 그래서 "Large Scale" , "Heterogeneous" 같은 엄청난 단어들이 논문 제목으로
* 따라서 TensorFLow 도 애초에 Session이라는 기존에 이미 구축되어 있는 cluster에 접속하는 형태로 ( 비록 간단한 모델일지라도 ) cluster에 모델을 초기화하고 Data를 feed 해서 학습하는 구조로 되어 있음
* 분산 아키텍쳐는 PS( parameter server ) , WORKER( computing ) 으로 분리 될 수 있고 위 노드간 통신을 위해 grpc를 사용하고 직렬화를 위해 protobuf를 사용
* Model Parallel , Data Parallel , Synchronous / Asynchronous Parallelism
