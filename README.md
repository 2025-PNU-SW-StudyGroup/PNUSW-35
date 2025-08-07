### 1. 프로젝트 소개
이 레파지토리는 참여자들이 학습공동체 결과물을 위한 레파지토리 생성시에 참고할 내용들을 담고 있습니다.
1. 레파지토리 생성
2. 레파지토리 구성
3. README.md 가이드라인
4. README.md 작성팁
<br/>


## 1. 레파지토리 생성

- https://classroom.github.com/a/wUrpZB4m
- 위 Github Classroom 링크에 접속해 본인 조의 github 레파지토리를 생성하세요.
  <img src="https://github.com/user-attachments/assets/d82da173-34a9-4adf-82e6-b712c59ecc70" width="600px" alt="classroom에서 팀 생성 그림"/>
- 레파지토리 생성 시 팀 이름은 `{조번호}` 형식으로 생성하세요.
- 예를 들어, 3조의 팀명은 `03` 입니다.
- 이 경우 `PNUSW-03`이라는 이름으로 레포지토리가 생성됩니다.
- 팀원의 경우 생성되어 있는 팀에 참가해주세요. <br/>
  팀에 참가하지 않았을 경우, 레포지토리에 대한 권한이 없어 PR 및 commit이 막힐 수 있습니다.
  <img src="https://github.com/user-attachments/assets/e1eece39-9d07-485a-aadf-74479ee85d90" width="600px" alt="classroom에서 팀 참여 그림"/>
<br/>


## 2. 레파지토리 구성
- 레파지토리 내에 `README.md` 파일 생성하고 아래의 가이드라인과 작성팁을 참고하여 파일을 작성하세요.
- 레파지토리 내에 `docs` 폴더를 생성하고 폴더 내에는 과제 수행 하면서 작성한 각종 보고서, 발표자료를 올려둡니다.
- 그 밖에 레파지토리의 폴더 구성은 과제 결과물에 따라 자유롭게 구성하되 가급적 코드의 목적이나 기능에 따라 폴더를 나누어 구성하세요.  
<br/>


## 3. README.md 가이드라인
- README 파일 작성시에 아래의 5가지 항목의 내용은 필수적으로 포함해야 합니다.
- 아래의 7가지 항목이외에 프로젝트의 이해를 돕기위한 내용을 추가해도 됩니다.
- `SAMPLE_README.md`가 단순한 형태의 예제이니 참고하세요.
markdown

### 1. 프로젝트 소개
#### 1.1. 개발배경 및 필요성
> 최근 기후변화로 인해 국지적 집중호우가 빈번해지며, 산림 지역에서의 산사태 발생 위험이 증가하고 있는 추세이다. 특히 임도는 산사태의 주요 발생 지점으로, 임도 하부에 위치한 민가 약 1,900채가 직접적인 위험에 노출되어 있어 예상되는 피해의 규모가 크다. 그러나 인력과 예산의 부족으로 인해 임도 주변의 배수 체계가 미비하며, 산사태 발생 이후에도 방치되는 사례가 다수 존재한다. 이에 따라 임도 기반의 산사태 위험 예측 및 사전 예방 체계 구축이 시급한 과제이다.

#### 1.2. 개발 목표 및 주요 내용
> 본 프로젝트의 주요 목표는 임도 구간별 산사태 발생 빈도와 환경 요인 간의 관계를 분석하고, 이를 바탕으로 k-means 클러스터링을 활용하여 임도 유형을 군집화하며, 위험 유형을 정량적으로 도출하는 것이다. 이를 통해 고위험 임도를 식별하고, 향후 사방사업 우선 대상지 선정 및 산림재난 대응 계획 수립에 과학적인 데이터를 제공하고자 힌다. 또한, 위험 임도망도 분석을 통해, 산사태에 취약한 구간을 사전에 파악하고, 지역별 산림재난방지 시행계획의 수립을 위한 근거 자료로 활용하는 것을 목표로 한다.

#### 1.3. 세부내용
##### 사용한 데이터 

- 활용데이터 임도망도(shp): 임도의 노선, 시공년도, 거리 등
- 산사태위험지도(geoTiff): 전국 산림 10mx10m 격자별 산사태 위험 등급
- 산림토양도(shp): 지형과 토양 특성을 '토양형' 단위로 제공
- 임상도(shp): 임종, 임상, 수종, 영급, 수관밀도 등 산림 분포 정보
- 산사태 발생 이력(csv): 피해원인, 피해주소, 피해면적 등 기록
- 산지 경사도(shp): 경사도 분석 서비스 데이터
- 강수량(csv): 방재기상관측 월강수량 합계

##### 분석 및 군집화

임도 버퍼 크기(폭 10m,)에 오버랩 되는 부분의 공간 데이터를 추출, 산사태 발생 유무 및 빈도를 반영한 피처 엔지니어링 수행

k-means 클러스터링을 통해 임도의 위험 유형을 분류

산사태와 상관관계가 높은 요인 분석 (예: 경사도, 강수량, 수종 등)

시각화 및 정책 제언

위험도에 따라 색상별로 임도망을 시각화하여 직관적 전달

고위험 군집에 속하는 임도를 사방사업 우선 대상지로 추천

지자체별 산림재난방지계획 수립 시 과학적 근거 자료 제공

#### 1.4. 기존 서비스 대비 차별성
> 기존 서비스 대비 차별성 

#### 1.5. 사회적가치 도입 계획
> 위 내용을 작성하세요.


### 2. 상세설계
#### 2.1. 시스템 구성도
> 시스템 구성도(infra, front, back등의 node 간의 관계)의 사진을 삽입하세요.

#### 2.1. 사용 기술
> 스택 별(backend, frontend, designer등) 사용한 기술 및 버전을 작성하세요.
> 
> ex) React.Js - React14, Node.js - v20.0.2

### 3. 개발결과
#### 3.1. 전체시스템 흐름도
> 위 내용을 작성하세요.

#### 3.2. 기능설명
> 각 페이지 마다 사용자의 입력의 종류와 입력에 따른 결과 설명 및 시연 영상.
> 
> ex. 로그인 페이지:
> 
> - 이메일 주소와 비밀번호를 입력하면 입력창에서 유효성 검사가 진행됩니다.
> 
> - 요효성 검사를 통과하지 못한 경우, 각 경고 문구가 입력창 하단에 표시됩니다.
>   
> - 유효성 검사를 통과한 경우, 로그인 버튼이 활성화 됩니다.
>   
> - 로그인 버튼을 클릭 시, 입력한 이메일 주소와 비밀번호에 대한 계정이 있는지 확인합니다.
>   
> - 계정이 없는 경우, 경고문구가 나타납니다.
>
> (영상)

#### 3.3. 기능명세서
> 개발한 제품에 대한 기능명세서를 작성해 제출하세요.
> 
> 노션 링크, 한글 문서, pdf 파일, 구글 스프레드 시트 등...

#### 3.4. 디렉토리 구조
> 위 레포지토리의 디렉토리 구조를 설명하세요.

### 4. 설치 및 사용 방법
> 제품을 설치하기 위헤 필요한 소프트웨어 및 설치 방법을 작성하세요.
>
> 제품을 설치하고 난 후, 실행 할 수 있는 방법을 작성하세요.

### 5. 소개 및 시연 영상
> 프로젝트에 대한 소개와 시연 영상을 넣으세요.
> 프로젝트 소개 동영상을 교육원 메일(swedu@pusan.ac.kr)로 제출 이후 센터에서 부여받은 youtube URL주소를 넣으세요.

### 6. 팀 소개
> 팀원 소개 & 구성원 별 역할 분담 & 간단한 연락처를 작성하세요.

### 7. 해커톤 참여 후기
> 팀원 별 해커톤 참여 후기를 작성하세요.
```
<br/>


## 4. README.md 작성 팁
- 마크다운 언어를 이용해 README.md 파일을 작성할 때 참고할 수 있는 마크다운 언어 문법을 공유합니다.
- 다양한 예제와 보다 자세한 문법은 [이 문서](https://www.markdownguide.org/basic-syntax/)를 참고하세요.

### 4.1. 헤더 Header
```
# This is a Header 1
## This is a Header 2
### This is a Header 3
#### This is a Header 4
##### This is a Header 5
###### This is a Header 6
####### This is a Header 7 은 지원되지 않습니다.
```

# This is a Header 1
## This is a Header 2
### This is a Header 3
#### This is a Header 4
##### This is a Header 5
###### This is a Header 6
####### This is a Header 7 은 지원되지 않습니다.
<br />

### 4.2. 인용문 BlockQuote
```
> This is a first blockqute.
>	> This is a second blockqute.
>	>	> This is a third blockqute.
```
> This is a first blockqute.
>	> This is a second blockqute.
>	>	> This is a third blockqute.
<br />

### 4.3. 목록 List
* **Ordered List**
```
1. first
2. second
3. third  
```
1. first
2. second
3. third
<br />

* **Unordered List**
```
* 하나
  * 둘

+ 하나
  + 둘

- 하나
  - 둘
```
* 하나
  * 둘

+ 하나
  + 둘

- 하나
  - 둘
<br />

### 4.4. 코드 CodeBlock
* 코드 블럭 이용 '``'
```
여러줄 주석 "```" 이용
"```
#include <stdio.h>
int main(void){
  printf("Hello world!");
  return 0;
}
```"

단어 주석 "`" 이용
"`Hello world`"

* 큰 따움표(") 없이 사용하세요.
``` 
<br />

### 4.5. 링크 Link
```
[Title](link)
[부산대 소프트웨어융합교육원](https://swedu.pusan.ac.kr/swedu/index.do)

<link>
<https://swedu.pusan.ac.kr>
``` 
[부산대 소프트웨어융합교육원](https://swedu.pusan.ac.kr)

<https://swedu.pusan.ac.kr>  
<br />

### 4.6. 강조 Highlighting
```
*single asterisks*
_single underscores_
**double asterisks**
__double underscores__
~~cancelline~~
```
*single asterisks* <br />
_single underscores_ <br />
**double asterisks** <br />
__double underscores__ <br />
~~cancelline~~  <br />
<br />

### 4.7. 이미지 Image
```
<img src="/path/to/img.jpg" width="600px" title="Title" alt="Alt text"></img>
![Alt text](/path/to/img.jpg "Optional title")
```
<img src="https://github.com/pnuswedu/SW-Hackathon-2024/assets/34933690/be7beb64-490f-4480-b121-f25cde7f2a8d" width="600px" title="부산대학교 소프트웨어융합교육원" alt="부산대학교 소프트웨어융합교육원"></img>
<br/>
![부산대학교 소프트웨어융합교육원](https://github.com/pnuswedu/SW-Hackathon-2024/assets/34933690/884154bb-28f6-4498-9f64-a8a878972951, "부산대학교 소프트웨어융합교육원")
<br/>

















