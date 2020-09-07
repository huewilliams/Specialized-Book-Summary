# 1장 애자일 개발 방법론

소프트웨어는 사람이 하는 일이다. 하나의 소프트웨어를 개발하기 위해서는 요구 사항을 분석해서 디자인하고, 이 디자인을 나눠서 개발자들이 각자 개발을 진행한다. 개발된 컴포넌트는 테스트 되고 마지막에는 서로 합쳐져서 하나의 유기적인 시스템을 이룬다. 이러한 개발 과정을 `개발 프로세스`라고 하고 여기에 조직 구조와 도구 셋을 포함하여 `개발 방법론`이라고 정의한다.

소프트웨어 개발 방법론은 폭포수 방식의 개발 모델부터 애자일 방식까지 계속해서 진화해 왔는데, 이 진화의 핵심은 **실제 개발에 얼마나 효율적으로 적용하여 품질 높은 소프트웨어를 만들 수 있는가**이다. 폭포수 모델이나 IBM의 RUP 같은 방법론들은 복잡도가 높고 실제 프로젝트의 개발 프로세스와 차이가 크다.

소프트웨어 개발이 요구 사항과 개발자의 실력이 변화가 있음을 전제로 하고, 변화를 수용하는 형태로 개발 프로세스를 변경하고, 개발을 하는 주체들이 이해하고 효율적으로 사용할 수 있는 방법론인 `실용주의 방법론(Practical Methodology)`가 대두되었다. 실용주의 방법론의 특징은 다음과 같다.

* 변화를 수용한다.
* 개발 과정을 짧은 조각으로 나누어서 반복적으로 개발한다.
* 소프트웨어에 결함이 있음을 전제로 한다.
* 문서 작업을 최소화한다.
* 협업과 커뮤니케이션에 많은 비중을 할애한다.
* 자동화 도구를 사용한다.

합리적이긴 하지만 소프트웨어 개발 프로젝트의 관리자 입장에서는 어려움이 있다. 프로젝트의 `일정 통제`를 위해 전체 프로젝트 기간이 프로젝트 초기부터 세트업되어 단계별로 관리가 되어야 하지만, 실용주의 방법론은 프로젝트 기간 중에 범위나 일정을 변경하므로 통제가 어렵다. 따라서 엔터프라이즈 프로젝트를 위해 적용할 수 있는 `변형된 스크럼 방법론`과 함께 일반적인 서비스 개발에 적합한 JIRA를 이용한 `일반적인 스크럼 개발 방법론`으로 나누어 알아본다.

## 1. 애자일 개발 방법론 <a id="3bdbcc88-8bb8-4177-a309-b345ed51c046"></a>

실용주의 방법론에서 소프트웨어 개발 프로세스는 `애자일`을 바탕으로 구성된다. 이 방법론의 특징은 구성원 간의 `협업 (Collaboration)`을 중요시하는 사상을 가지고 있다. 애자일 방법론에는 **XP\(Extreme Programming\), AUP\(Agile Unified Process\), 스크럼, Lean, 칸반** 등 여러 가지 구체적인 방법론들이 있는데, 그중에서 `스크럼`이 가장 많이 사용된다.

### 빅 엄브렐라\(Big Umbrella\) 방법론 <a id="5a3da52a-5e44-4317-b4ba-1465ade871c5"></a>

조직에서 사용하는 전통적인 개발 프로세스를 사용하여 전체 프로세스에 대한 관리성을 확보하고, 단계별 개발은 스크럼 방법론을 적용한 방법론을 `빅 엄브렐라 방법론`이라 정의한다. 예를 들어 전사 개발 방법론을 폭포수 모델을 사용할 때 각 단계에 대해서 반복 기반으로, 분석-설계-개발-테스팅을 반복한다.

### 1.1 빅 엄브렐라 방법론의 팀 구조 <a id="20b1f1b5-bb9f-4db9-9478-1fccfbe1f1bd"></a>

* `프로젝트 매니저(PM)` : 전체 프로젝트를 관리하는 역할. 전통적인 개발 프로세스를 기준으로 프로젝트를 관리하며 애자일 방법론과 기존 개발 프로세스를 연계시키는 역할을 맡는다.
* `프로젝트 리더(PL)` : 실제 개발팀을 가지고 구현을 리드하는 사람이다. 실제로 애자일 프로세스를 이용하여 팀의 작업을 관리한다.
* `애자일 코치` : 스크럼 마스터, 팀의 프로세스를 세트업하고 팀이 프로세스를 준수하도록 코칭, 개선하는 역할을 한다. 애자일 프로세스를 적용할 때 성숙 단계까지\(약 2개월\) 지속적인 관찰과 코칭이 필요하다.

## 2. 전통적인 스크럼 개발론 <a id="a6f92ef4-6f23-4f9c-92a1-e9980cbc25cc"></a>

`스크럼`은 기본적으로 `반복과 점진적` 개발 방법에 기초한다.

스크럼은 몇 개의 이터레이션으로 구성되는데, 이 이터레이션을 `스프린트`라고 부르며 각 스프린트는 1~4주의 기간을 갖는다. 한번 정해진 스프린트 기간은 변경될 수 없음을 전제로 한다.

스크럼에는 고객의 요건으로부터 작성된 `제품 백로그(Product Backlog)`라는 것이 있다. 요구사항정의서\(SRS\), 기술요구사항 정의서\(TRS\)에 정의된 기능이나 구현 요구 사항이 제품 백로그 항목으로 적절하다.

이 제품 백로그 항목을 팀 미팅을 통해 이번 스프린트에 수행할 항목을 제품 백로그 항목의 `우선순위`를 통해 선택되고, 이 선택된 항목들을 구체적으로 구현하기 위해 `태스크`로 쪼게 진다. 선택된 백로그 항목 리스트를 `스프린트 백로그(Sprint Backlog)`라고 부른다.

스프린트 백로그의 태스크들은 스케줄이 지정되어 팀의 담당자에게 `할당(Assign)`된다. 팀은 스프린트 백로그를 가지고 정해진 기간동안 스프린트를 구현한다.

스프린트 중에 매일 아침 팀원들은 10~20분 정도의 `일일 스크럼 미팅(Daily Scrum)`이라는 회의 시간을 가진다. 이 시간 동안, 팀원들은 어제 한 일과 오늘 할 일에 대해 간략히 보고하고 문제점을 공유한다.

스프린트가 끝나면 해당 소프트웨어를 `릴리즈`한다. 릴리즈 후에는 이해 당사자와 리뷰 미팅을 가져 피드백을 받아 제품 백로그에 업데이트하고 다음 스프린트를 준비한다.

리뷰 후에는 팀원끼리 스프린트에 대한 `회고(Retrospective)`의 시간을 가져 팀의 스크럼 운영 방식을 성숙화시킨다.

### 2.1 스크럼 방법론에서 역할 <a id="207d1089-ede9-4ae4-9a07-751fc6565bc6"></a>

* `제품 오너` : 재퓸 오너는 요구 사항을 정의하고, 제품 백로그를 업데이트하는 역할을 맡고 있다. 제품 백로그 내의 항목에 대한 우선순위를 조정하는 역할도 맡는다. 제품 오너는 직접 스프린트에 참여하며, 비즈니스쪽과 지속적으로 의사소통하면서 요구사항을 구체화하고 기능의 우선순위를 조정해서 팀에게 명확한 방향성을 제공한다. 제품 오너는 중요한 의사 결정을 해야 하는 경우가 많으므로 적절한 권한과 충분한 시간이 주어져야 한다. 제품 오너는 제품에 대한 기능을 정의해야 하므로 제품 도메인에 대한 충분한 지식이 있어야 한다.
* `스크럼 팀` : 팀은 제품 백로그의 내용에 따라 스프린트를 수행하는 역할을 한다.
* `스크럼 마스터` : 해당 프로젝트에 대한 일정과 태스크를 조율하는 역할을 한다. 또한 스크럼 방법론을 팀에 전파하고 적용하는 책임을 갖는다.

### 2.2 스크럼에서 에픽과 사용자 스토리 <a id="799db796-2c7a-477f-aeab-5572db9be54d"></a>

`사용자 스토리`는 요구 사항에 해당하며 흔히 "as a user, I want to upload photo"라는 식으로, 액터\(Actor, 사용자\)와 액터의 행위를 서술하는 형태가 된다.

이러한 사용자 스토리를 큰 단위\(사진 업로드, 사진 리스트\)로 묶어 놓은 것을 `에픽`이라고 한다.

사용자 스토리는 이를 구현하기 위해 몇 개의 `태스크`로 나누어진다.

## 3. 엔터프라이즈 개발을 위한 스크럼 기반의 개발 방법론 <a id="53d8a7c1-5c33-4d10-a3d6-8f91cbe6fa3e"></a>

여기서 설명하는 방법론은 스크럼을 기반으로 해서 `관리 지향적`인 엔터프라이즈 소프트웨어 개발에 맞도록 발전시킨 형태의 소프트웨어 개발 방법론이다. 기존 스크럼과의 차이로 좀 더 관리지향 적인 관점에서 접근하여 프로젝트의 진행 상황에 대한 `가시성`을 확보하는 데 목적을 둔다.

### 3.1 제품 백로그 준비 <a id="a336c9f7-d309-4827-8510-a7f6bf7d7792"></a>

제품 백로그는 실제로 구현되어야 하는 기능 목록을 나열한다. 목록은 고객의 `요구사항`으로부터 도출 되는데, 일반적으로 요구사항 정의서\(SRS\)나 기술요구사항 정의서\(TRS\)로부터 도출된다. 제품 백로그의 항목은 다음과 같다.

1. 번호 : 기능에 대한 ID
2. 항목 제목
3. 설명
4. 예측 소요 시간
5. 요건 설명 링크
6. 우선순위
7. 상태
8. 항목에 대한 비즈니스 가치 \[선택 사항\]

### 3.2 릴리즈 계획 <a id="2aa6cb27-502b-461f-a55d-35da49e90345"></a>

제품 백로그가 정의되었으면, 언제 어떤 일을 해야 할지를 정의해야 한다. `릴리즈 계획`에서는 프로젝트의 큰 **마일스톤\(Mile Stone\)**을 정하는 작업을 한다. 릴리즈된 시점에서 QA팀에게 품질을 검증받고 릴리즈된 버전을 고객에데 데모를 통해 요구사항과 부합하는지 확인 할 수 있다. 이 단계의 구체적인 작업은 다음과 같다.

1. 주요 릴리즈 일정 지정
2. 릴리즈 일정별로 포함할 제품 백로그 내의 항목 지정

### 3.3 스프린트 계획 <a id="b36e69ec-219a-4777-9565-e42fec7e3142"></a>

릴리즈 계획이 끝난 후에는 각 릴리즈를 달성하기 위해 각 중요 마일 스톤을 작은 스프린트 단위로 쪼갠다. 다음과 같은 절차로 `스프린트를 계획`한다. 스프린트는 보통 1~4주로 정의된다.

1. 팀원의 가용 시간 파악
2. 제품 백로그의 항목을 구체적인 태스크로 분할 \(태스크는 명확한 종료 조건이 있어야 한다.
3. 각 태스크를 프로젝트 리더인 스크럼 마스터가 적절한 사람에게 배분
4. 배분된 사람이 태스크의 수행 시간을 예측하도록 함

**1:1:1 법칙**

일반적으로 분석/설계, 구현, 테스트에 대한 리소스 할당 비율은 `1:1:1`이 된다.

**20% 버퍼의 법칙**

전통적인 스크럼 방식은 백로그에 앞으로 해야 할 일만 정의한다. 하지만 해야 할 일과 진행되고 있는 일이 언제 시작해서 언제 끝날 것인지에 대한 관리가 어렵다. 이 문제점을 해결하기 위해 태스크 별로 시작이라고 종료일을 지정하는 일종의 `WBS(Work Breakdown Structure)`의 개념을 사용해서 진행하는 일과 앞으로 해야 할 일의 일정을 추적할 수 있다.

### 3.4 스프린트 관리 <a id="29a8484b-3ee6-4691-ab48-ad533722bc17"></a>

`일일 스크럼(Daily Scrum)`

스크럼 팀은 매일 오전에 같은 자리에 모여서 어제 자신이 한 일과 오늘 자신이 해야 할 일을 짧게 발표한다. 이 과정에서 팀원은 다른 팀원의 태스크 진행 상황을 공유할 수 있고, 만약 일의 진행에서 문제가 있는 부분은 이슈로 제기하여 다른 사람의 도움을 요청하거나 PM이 일정을 조정할 수 있도록 한다. PM은 공유된 일정을 바탕으로 스프린트 백로그의 상세 태스크의 종료 시간까지 남은 시간을 업데이트한다.

`번 다운 차트(Burn Down Chart)`

스프린트 제품 백로그를 위와 같은 방법으로 업데이트하면 매일 남은 작업 일 수를 계산할 수 있는데, 이를 그래프로 표현한 것을 번 다운 차트라고 한다. 번 다운 차트를 매일 업데이트함으로써 이상 그래프에서 실제 프로젝트의 남아 있는 작업량이 그래프가 얼마나 벗어나는가를 측정함으로써 프로젝트의 일정상 위기 요소를 파악하고 대비할 수 있다.

`태스크 상태`

각 태스크에 대해 상태를 관리해야 한다. 항상 상태를 업데이트해서 팀원이나 운영 조직 간에 자주 의사소통 할 수 있고 저장된 상태나 값을 기반으로 여러 가지 지표를 뽑아 낼 수 있다. 태스크 상태는 태스크의 상태 흐름에 따라 정의되는데, 이를 **태스크 워크플로**라고 한다. 태스크 워크플로는 최대한 단순해야 하며, 적용되는 업무의 특성별로 잘 정의되어야 한다.

### 3.5 스프린트 종료 <a id="ba95f0a2-4f28-4d06-bdaa-4f3c185915eb"></a>

정해진 기간에 스프린트가 종료되면 스프린트를 정리한다. 스프린트 종료 조건은 팀에 따라 정할 수 있는데 크게 아래 조건을 많이 사용한다. 중요한 것은 명시적인 종료 조건을 정의해야 한다는 것이다.

* 정해진 시간
* 태스크 종료
* 예산 종료 시 까지

`스프린트 리뷰`

스프린트가 종료된 후에는 스프린트에서 구현된 산출물을 리뷰하는 단계가 필요하다. 요구사항을 적절하게 구현했는지, 품질은 만족했는지 등의 검증이 필요하다. 실제 구현 코드, 산출 문서, 테스트 결과 등 구체적인 자산을 가지고 리뷰를 수행해야 한다. 이 과정에서는 고객을 참여시켜서 자산에 대해서 간략한 데모를 고객에게 수행한다.

`테스트`

스프린트 계획에서 구현의 경우 테스트 작업을 반드시 포함시키고, 리뷰 과정에서는 이 테스트 결과를 리뷰하도록 한다. 테스트는 기능적 테스트 뿐만 아니라 안정성이나 성능 같은 비기능적 요건에 대한 테스트도 포함되어야 한다. 스크럼에 권장되는 테스트 구현은 다음과 같다.

* **단위 테스트\(Unit Test\)** : 개발자가 개발 컴포넌트 단위로 테스트 수행
* **회귀 테스트\(Regression Test\)** : 테스트했던 내용을 다음 테스트에 포함시켜 새로운 코드나 변경이 기존 기능에 영향을 주지 않는지 매번 검증
* **테스트 자동화\(Test Automation\)** : 테스팅의 효율성 극대화
* **점진적 통합\(Contiguous Integration\)** : 일일 빌드 등을 통해서 점진적 통합 전략을 사용함

### 3.6 제품 백로그 업데이트 <a id="cbb35eff-d74f-4cf0-ab8d-def507dafb03"></a>

리뷰가 끝났으면 리뷰 과정에서 나온 추가 요건이나 변경 상황을 반영하여 제품 백로그를 업데이트한다. 팀이 모여서 우선순위, 요구사항, 예상 소요 시간을 업데이트 한다.

### 3.7 회고\(Retrospective\) <a id="79be677f-2a01-4db3-a527-6bb0ccffab0d"></a>

스프린트가 종료되고 모든 작업이 끝나면 팀에서 운영 중인 방법론 자체에 대한 리뷰가 필요하다. 스프린트 경험을 기반으로 회고를 수행함으로써 프로세스를 발전시킬 수 있는 방향을 찾을 수 있다.
