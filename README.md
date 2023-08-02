# AWS Sagemaker를 이용한 MLOps와 LLMOps

안녕하세요? 서진호입니다. 

이번 주 AWSKR USER GROUP 의 데이터 모임 에서 발표한 자료를 공유해 드립니다.
주제는 "AWS Sagemaker를 이용한 MLOps 와 LLMOps" 로 2시간 정도 발표한 자료입니다.
그날 많은 분들이 질문을 주셔서 그것을 반영해서 좀더 추가적인 자료를 넣어서 작성했습니다.

제 1 부에서는 다음과 같은 내용으로 발표했습니다.

<p> • MLOps (AI/ML lifecycle) 및 AI/ML Stack • AWS SageMaker 2022.12 주요 기능 </p>
<p> • SageMaker Domain 및 User Profile • SageMaker Projects – Pipeline </p>
<p> • SageMaker Notebooks </p>
<p> • SageMaker Studio </p>
<p> • SageMaker Processing (전처리) </p>
<p> • SageMaker Autopilot (AutoML) </p>
<p> • SageMaker Training Jobs </p>
<p> • SageMaker Experiments 및 Trials </p>
<p> • SageMaker Serving and Deployment 
<p> • SageMaker Endpoints </p>
<p> • SageMaker Debugger </p>
<p> • SageMaker Monitor </p>
<p> • 실습: SageMaker Notebooks 에서 ML 모델을 ECR 배포 및 엔드포인트 </p>


제 2 부에서는 다음과 같은 내용으로 발표했습니다.

<p> • 생성 AI과 초거대 언어 모델(LLM) </p>
<p> • 생성 AI 생태계 </p>
<p> • 생성 AI 사용사례와 분야별 랜드스케이프 </p>
<p> • 초거대 언어 모델(LLM) 진영 </p>
<p> • 허깅 페이스 오픈 LLM 리더보드 </p>
<p> • MS/OpenAI 공동 전략, 구글 BARD(PaLM2) 과 AWS 생성 AI 전략 </p> 
<p> • LLM 기술 구조 – LLM 정의와 LLM 파운데이션 모델 </p>
<p> • 비공개 소스 GPT3 vs. 공개 소스 메타 LLaMA </p>
<p> • 오픈 소스 프레임워크: Auto-GPT 와 LangChain </p>
<p> • 국내 LLM 히스토리 – 한글 데이터셋 </p>
<p> • 생성 AI 애플리케이션 방법론 </p>
<p> • 초거대 언어 모델(LLM) 생명주기 </p>
<p> • 초거대 언어 모델(LLM) 아키텍처 </p>
<p> • LLM 프롬프트 및 태스크 </p>
<p> • 추론을 위한 생성형 환경 설정 파라미터 </p>
<p> • LLM 프롬프트 및 태스크 </p>
<p> • LLMOps 와 LLM 모델 개발 조언 </p>

그리고 demo_code 폴더에 관련 예제 소스를 수록했고, 소스에 주석을 달아 놓았습니다. 
혹시 작동시켜 보시다가 안되시면 언제든지 저에게 메일을 주시면 답변 드리도록 하겠습니다.

## Further Readings ##

<P> * AWS 로그 </P>

1. [Amazon Bedrock용 에이전트 미리보기 출시](https://aws.amazon.com/ko/blogs/korea/preview-enable-foundation-models-to-complete-tasks-with-agents-for-amazon-bedrock/): 채팅 서비스보다 Autogpt 처럼 에이전트로 멀티 엄무 태스크(Advanced Reasoning and ReAct)를 LLM에게 전달하고 연속 업무를 하기 위한 AWS 서비스, 현재는 프리뷰 서비스라 사용하려면 별도로 신청해야 함.    

2. [Introducing the vector engine for Amazon OpenSearch Serverless, now in preview](https://aws.amazon.com/ko/blogs/big-data/introducing-the-vector-engine-for-amazon-opensearch-serverless-now-in-preview/): OpenSearch 를 이용한 벡터 데이터베이스 임베딩과 증강된 ML 검색


<p> * 읽어 보시면 유용할 만한 LLM 관련 논문, 기사, 블로그 </p>

1. [Llama 2: Open Foundation and Fine-Tuned Chat Models](https://arxiv.org/pdf/2307.09288.pdf): LLaMa2 파운데이션 모델의 아키텍처와 구조에 대해 알 고 파인튜닝할 수 있는 논문.
2. [Introducing the Hugging Face LLM Inference Container for Amazon SageMaker](https://huggingface.co/blog/sagemaker-huggingface-llm): 세이지메이커에서 Jumpstart 외에 Hugging Face를 바로 이용해서 추론 컨테이너를 생성하고 빌드시키는 법.
3. [Efficient Training on Multiple GPUs](https://huggingface.co/docs/transformers/v4.31.0/en/perf_train_gpu_many): 멀티 GPU 상에서 효율적인 훈련 방법과 종류에 대한 설명.
4. [Hugging Face - Accelerate](https://huggingface.co/docs/accelerate/index): Accelerate는 단 4줄의 코드만 추가하여 모든 분산 구성에서 동일한 PyTorch 코드를 실행할 수 있게 해주는 허깅페이스의 라이브러리인 Accelearate 추론과 훈련 설명함.
5. [Hugging Face - Fully Sharded Data Parallel](https://huggingface.co/docs/accelerate/usage_guides/fsdp): 더 큰 배치 사이즈가 큰 LLM을 빠르게 훈련하기 위해 완전히 분할된 데이터 병렬 모델(FSDP)을 사용하는 방법을 PyTorch로 구현. 이러한 유형의 데이터 병렬 패러다임은 옵티마이저 상태, 그래디언트 및 파라미터를 샤딩하여 더 많은 데이터와 더 큰 모델에 맞출 수 사용할 수 있음. 
6. [QLoRa: Fine-Tune a Large Language Model on Your GPU](https://towardsdatascience.com/qlora-fine-tune-a-large-language-model-on-your-gpu-27bed5a03e2b): GPU를 가지고 LLM을 파인튜닝할 때 QLoRa 를 사용하면 성능도 향상되고 비용도 줄일 수 있음. 
7. [ReLoRa: Pre-train a Large Language Model on Your GPU](https://towardsdatascience.com/relora-pre-train-a-large-language-model-on-your-gpu-d104756f9ddf): LoRA에서 파라미터를 그대로 유지하고 Low Rank를 추가해서 비용을 줄일 수 있는 최신 방법 제안
8. [Lost in the Middle: How Language Models Use Long Contexts](https://arxiv.org/pdf/2307.03172.pdf): LLM이 프롬프트 상에서 매우 큰 컨텍스트가 주어졌을 때 정보가 중간 부분에 묻혀 관련 정보를 추출하는 데 어려움을 겪음. 따라서, RAG(Retrieval Augmented Generation) 형식의 검색 시스템으로 관련 정보를 대규모로 추출하도록 특별히 설계되어 비용이 크게 절감되었다는 내용. 이때 벡터 데이터베이스를 사용하면 유용. 
9. [DeepSpeed ZeRO++: A leap in speed for LLM and chat model training with 4X less communication](https://www.microsoft.com/en-us/research/blog/deepspeed-zero-a-leap-in-speed-for-llm-and-chat-model-training-with-4x-less-communication/): DeepSpeed ​​ZeRO++: 4배 적은 커뮤니케이션으로 LLM 및 채팅 모델 교육 속도 향상
10. [팀 데트머스 - 딥 러닝에서 GPU 사용에 대한 나의 경험 및 조언](https://timdettmers.com/2023/01/30/which-gpu-for-deep-learning/): 딥러닝에서 GPU 사용에 대한 나의 경험 및 조언으로 GPU 사용할 때 고려할 점을 알 수 있음.
11. [Running Llama 2 on CPU Inference Locally for Document Q&A](https://towardsdatascience.com/running-llama-2-on-cpu-inference-for-document-q-a-3d636037a3d8): 로컬에서 LlaMa 2를 CPU 추론하는 방법
12. [Frameworks for Serving LLMs](https://slgero.medium.com/frameworks-for-serving-llms-60b7f7b23407): LLM을 서빙할 때 다양한 방법들을 소개함. 현재로는 vLLM 프레임워크가 가장 빠름.

