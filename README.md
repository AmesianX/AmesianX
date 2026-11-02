### AmesianX

공격 연구와 로컬 LLM. 만든 것들을 주제별로 묶어 둡니다.
핀은 6개가 상한이라 나머지는 여기에 적습니다.

#### 로컬 LLM · 추론

텔레그램 봇 풀을 등록해 두면 원격 제어가 완벽하게 지원되며, 이미지 인식 기능까지 제공됩니다. 특히 이미지 식별 성능이 매우 뛰어납니다.
만약 자신의 방 안에 클로드 코드 오퍼스를 구축해 두고 싶다면, 이 세팅을 강력히 추천합니다.
검열 제한을 자동으로 해제하는 기능까지 지원해 레드팀 목적의 활용에서도 높은 효율을 기대할 수 있습니다.
이 프로그램은 무려 1년 6개월에 걸쳐 지속적으로 개발하고 다듬어 왔습니다.
모델 선택에 있어서는 DeepSeek 4.0 Flash는 절대 추천하지 않습니다. 제가 추천하는 모델은 단연 GLM 5.3 Flash입니다.
직접 사용해 보면 그 차이를 확실히 체감할 수 있을 것입니다.
DeepSeek 4.0 Flash에서 고질적으로 발생하던 반복 증상을 GLM 5.3 Flash에서는 발생하지 않도록 개선하는 데 성공했습니다.
혹시 반복 증상이 발생하더라도 즉시 감지하고 바로잡을 수 있는 보정 기술을 별도로 적용했습니다.
나아가 GLM 5.3 Flash 자체의 관련 버그까지 수정하여, 최종적으로 반복 증상 발생 횟수를 0회로 만드는 데 성공했습니다.
(윈도우에서도 잘 작동함)
| | |
|---|---|
| [**codemason**](https://github.com/AmesianX/codemason) | 로컬 LLM으로 도는 터미널 코딩 에이전트 CLI (Rust) / 체감 성능 클로드 코드 오퍼스 4.8 급 |
| [**codemason-py**](https://github.com/AmesianX/codemason-py) | 같은 구현의 Python 판 / 체감 성능 클로드 코드 오퍼스 4.8 급 |
| [**dspark-serve**](https://github.com/AmesianX/dspark-serve) | GLM-5.3-Flash EXL3 를 DGX Spark 2노드 vLLM 으로 서빙 (TP=2, 512K) / 체감 성능 클로드 코드 오퍼스 4.8 급 |
|---|터보퀀트 구현은 아쉽게도 최종 실패작입니다. 구현은 어느정도 되어있으나 llama.cpp 엔진의 한계에 봉착하여 폐기함|
| [**TurboQuant**](https://github.com/AmesianX/TurboQuant) | llama.cpp KV 캐시 압축 — 메모리 5.2배 |

#### 사설 5G

| | |
|---|---|
| [**private-5g-lab**](https://github.com/AmesianX/private-5g-lab) | 사설 5G SA 랩 — Open5GS + IMS(VoNR) + srsRAN/B210, 실물 단말 검증 / 핸드폰에 직접 전화걸기(통화) 성공 |
| [**local-5g-handbook**](https://github.com/AmesianX/local-5g-handbook) | 로컬 5G 망 구축하기 — 해커를 위한 이동통신 실무서 |

#### 취약점 연구

| | |
|---|---|
| [**CVE-2026-53435**](https://github.com/AmesianX/CVE-2026-53435) | 공격 연구자 + AI vs 갓 나온 n-day |
| [Chrome_Issue992914](https://github.com/AmesianX/Chrome_Issue992914) | Exodus Intelligence Chrome 익스플로잇의 32비트 윈도우 포팅 |

#### 도구

| | |
|---|---|
| [**amesianx-proxy**](https://github.com/AmesianX/amesianx-proxy) | 바이너리 프로토콜 분석용 범용 인터셉팅 프록시 |
| [softwire](https://github.com/AmesianX/softwire) | 버텍스 셰이더를 에뮬레이션하는 명령어 어셈블러 (지켜야 할 고전 유산이라고 생각해서 오래전부터 모아 둔 것) |

<sub>보안·기술 뉴스와 공개 PoC 를 한국어로 모으는 곳 — <a href="https://powerhacker.net">powerhacker.net</a></sub>
