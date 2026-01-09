---
{"dg-publish":true,"permalink":"/캠브리안 매뉴얼 홈페이지/캠브리안 UI 메뉴얼/","tags":["gardenEntry"]}
---


# 개요

Cambrian VISION은 Cambrian Vision 시스템을 위한 프로그램입니다. 
이 프로그램은 "임베디드"처럼 동작하며, Cambrian PC가 부팅될 때 자동으로 실행됩니다.
Cambrian Vision UI의 다양한 요소와 사용법에 대한 자세한 내용은 이 페이지에서 확인할 수 있습니다.

Cambrian VISION 2.x 이상의 버전은 차세대 버전입니다.
이 버전에서는 다음과 같은 기능을 지원합니다.
 - 기존의 "Grasp Point"방식 - 학습 전에 Grasp Point를 정의해야 합니다.
 - 새로운 "Full Pose"방식 - 모델 학습 후에 Grasp Point를 정의할 수 있습니다.
이 소프트웨어 버전은 두 가지 방식을 모두 지원하므로, 선택한 모델에 따라 사용자 인터페이스에 일부 차이가 있습니다.

![files/캠브리안 UI 메뉴얼/image.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/image.png)

---

# 학습된 모델 설치하기
Cambrian VISION은 사용하려는 부품에 맞는 학습된 AI 모델 파일이 필요합니다.
학습된 모델을 일반적으로  USB를 통해 Cambrian PC로 옮기거나, 제공된 다운로드 링크에서 직접 다운로드할 수 있습니다.
".CambrianAIModel"파일을 더블 클릭하면 PC에 모델이 자동적으로 설치됩니다.

![files/캠브리안 UI 메뉴얼/image-1.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/image-1.png)

> [!warning] 주의사항
> - 파일이 반드시 Cambrian PC로 완전히 복사되었는지 확인하세요.
> - USB 드라이브에서 직접 설치하는 것은 지원되지 않습니다.
> - 파일 이름에 번호가 매겨진 확장자가 포함되어 있는지 확인하세요
> 	- ex) "modelname (1).CambrianAIModel"
> - 같은 파일을 두 번 이상 다운로드 할 경우 이런 이름이 생길 수 있습니다.

설치된  AI 모델은 `~/Desktop/Caint/Networks`폴더에서 확인할 수 있습니다.
여기서 폴더 이름을 변경하면 모델의 이름을 바꿀 수 있습니다.

---
# 로봇 & 3D 환경
소프트웨어는 상호 작용이 가능한 뷰를 가지고 있으며, CAD 설계 소프트웨어에서 사용하는 3D 툴과 유사한 방식으로 작동합니다.

CAD 모델을 마우스를 사용하여 회전, 이동, 크기 조절이 가능합니다.
- 스크롤 휠 : 물채 확대 / 축소
- 오른쪽 클릭 + 이동 : 물체 회전
- 휠 클릭 + 이동 : 물체 이동

키보드 단축키
- F11 :  전체 화면 모드 전환
- ESC : 모든 팝업 메세지 닫기

---

# 상단 바(Top Bar)

![files/캠브리안 UI 메뉴얼/image-2.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/image-2.png)

## System Online(스위치 / 표시등)
- Cambrian 시스템이 "Online" 상태일 때는 로봇 요청을 처리할 준비가 완료된 상태이며, UI의 많은 기능이 비활성화 됩니다.
- 시스템 설정을 변경할려면 반드시 "Offline" 상태로 전환해야 합니다.
- 시스템이 오프라인일 때는 외부 장치(로봇)에서 들어오는 모든 요청에 대해 오류로 응답합니다.

## Live Images(버튼)
- 실시간으로 보이는 카메라의 뷰를 켜거나 끕니다.

## Run Model(버튼)
- 현재 로드된 모델을 연속적으로 실행하며, 예측 결과를 화면에 표시합니다.

## Connection Status(연결 상태)
- Camaras : 카메라 모듈 및 로봇과의 활성 연결 여부를 표시합니다.
	- 초록색 : 연결됨
	- 빨간색 : 연결되지 않음

- Robot : 지원되는 로봇의 경우 로봇 연결 상태를 표시합니다.
	- 선택한 로봇이 미지원일 경우 항상 회색으로 표시됩니다.

## GPU Usage(GPU 사용량)
-  현재 사용 중인 GPU 메모리 용량을 표시합니다.

## RAM Usage(RAM 사용량)
- 현재 사용 중인 RAM 용량을 표시합니다.

---

# 사이드 패널(Side Panel)

사이드 메뉴의 버튼들은 다양한 설정을 위한 에디터 / 뷰를 엽니다.

## Settings(셋팅)

![files/캠브리안 UI 메뉴얼/image-3.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/image-3.png)

- Robot(드롭다운 리스트)
	- 사용 중인 로봇을 드롭다운 목록에서 선택할 수 있습니다.

- PC IP(문자열 입력)
	- `xxx.xxx.xxx.xxx` 형식의 입력란에 이 PC에 할당할 IP 주소를 입력합니다.
	- 이 IP 주소는 Ubuntu 네트워크 설정과 일치해야 합니다.
	- 만약 입력한 IP 주소가 실제 PC의 IP와 다를 경우, 다음과 같은 다이얼로그 나타납니다.
	 ![files/캠브리안 UI 메뉴얼/image-4.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/image-4.png)
	- "Update System IP"를 클릭하면, 모든 네트워크 인터페이스의 IP가 지정한 IP로 변경됩니다.
	- 만약 PC에 네트워크 인터페이스가 여러 개 있다면, Ubuntu 네트워크 설정 도구를 사용하여 IP를 직접 설정하는 것이 좋습니다.
	- 참고 : 로봇과 PC가 반드시 동일한 서브넷에 있어야 합니다.

- Port(정수 입력)
	- Cambrian Vision UI가 로봇으로부터 요청을 받을 때 사용하는 TCP/IP 포트입니다.
	- 기본값은 4000이며, <font color="#0070c0">로봇의 설정과 일치</font>해야 합니다.

- **UR 로봇 전용기능**
	- **Robot IP** : 로봇의 IP 주소를 표시합니다.
	- **Real Time Visualisation** :  실시간으로 로봇의 자세(포즈) 업데이트를 활성화/비활성화할 수 있습니다.

## Workspace(작업 영역)

이 섹션은 충돌 요소(예 : 부품이 담긴 빈(bin)이나 플랜지 부착물)를 정의하고 테스트하는 데 사용됩니다.
이러한 충돌 요소는 모델에서 최적의 후보를 결정할 때 예측 결과를 필터링하는 데 활용됩니다.

![files/캠브리안 UI 메뉴얼/image-5.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/image-5.png)

### 주요기능 설명
- 카메라 설정 :  카메라 리그 캘리브레이션 데이터에서 자동으로 결정되며, 해당 리그가 선잭된 상태로 표시됩니다. 필요한 경우 이 선택을 수동으로 변경할 수 있습니다.
- 월드 스페이스(World Space) : 로봇에 부착되지 않은 환경 구성 요소(부품용 빈, 벽, 기타 장애물 등)를 정의합니다.
- 플랜지 스페이스(Flange Space) :  로봇 플랜지에 부착된 요소를 설정합니다.

### 사용 방법
1. 구성 요소는 UI 또는 로봇 API를 통해 생성할 수 있습니다.
2. 편집을 위해 "Edit Workspace"버튼을 클릭하세요 (*시스템이 받드시 "오프라인" 상태여야 합니다.*)
3. 변경 완료후 "Save changes"로 편집 모드를 종료합니다.

### CAD 형상 가져오기(Importing a CAD geometry)
모든 구성요소 유형에 대해, 기존에 제공되는 오브젝트 라이브러리(이전 버전의 단순 박스 등)에서 선택하거나 CAD 형상을 라이브러리로 가져와서 새로 생성할 수 있습니다.
CAD 형상을 가져올 때는 올바른 단위를 선택하여 크기가 정확한지 받드시 확인해야 합니다.
한 번 라이브러리에 가져온 항목은 이후 세션에서도 계속 사용할 수 있습니다.

![CADComponents.gif](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/CADComponents.gif)

### 컴포넌트 조작(Maniplating compnents)

컴포넌트를 선택하거나 가져온 후에는, 이동 및 크기 조절 작업을 통해 조작할 수 있습니다.
그래픽 도구를 사용하면 이러한 조작을 쉽게 할 수 있으며, 이는 그랩 포인트 편집 도구와 동일한 방식으로 작동합니다.
그래픽 기즈모는 선택한 에디터 필드에 따라 이동, 회전, 크기 조절 모드로 전환됩니다.
편집 가능한 필드는 mm 단위로 입력합니다.
가져온 CAD 컴포넌트는 크기 조절이 불가능하지만, 내장된 "geometric" 컴포넌트는 크기조절이 가능합니다.

![manupulating.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/manupulating.png)

리스트에서 컴포넌트를 선택하면 추가 수정 또는 삭제할 수 있습니다.

![modification.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/modification.png)

- + 표시 : 항목을 라이브러리로 가져오거나 라이브러리에서 삭제할 수 있으며, 항목을 "Add"하면 구성 요소 목록에 항목이 추가됩니다.
- x 표시 : 구성 요소를 제거합니다. 라이브러리에는 여전히 존재하지만, 이 세션에서는 제거됩니다.
- v 표시 : 구성 요소를 비활성화/활성화합니다. 비활성화된 구성 요소는 충돌 검사에서 무시됩니다.

### 도달 가능성 검증(Reachability checks)
로봇 환경 설계에서 흔히 발생하는 문제 중 하나는 로봇의 운동학적 한계나 플랜지 구성 요소와의 충돌로 인해 특정 위치에 도달하지 못하는 경우입니다.
Cambrian Vision은 이 문제를 해결하기 위해 "reachability" 테스트 기능을 제공합니다.
월드 컴포넌트를 선택한 상태에서 이 테스트를 실행하면, 해당 공간 내 여러 샘플 포인트들이 표시되며 각 위치의 도달 가능 여부가 색상으로 구분됩니다.
<font color="#00b050">초록색 점</font>이 최대한 많은 영역을 확보하도록 설계를 최적화할 수 있습니다.

주요기능
	- 컴포넌트의 방향이나 위치가 변경될 때마다 테스트가 자동으로 재실행됩니다.
	- 테스트 실행 시 TCP 편집기가 표시되면, 이 도구를 통해 장치의 TCP(Tool Center Point)를 정의하여 실제 작업 환경을 반영한 테스트가 가능합니다.

>[!tip] 참고 사항
>- <font color="#d83931">빨간색 점</font>은 플랜지 구성 요소, 카메라 리그, 로봇 암과 월드 컴포너는 간의 잠재적 충돌을 나타냅니다.
>- 실제 작동 시 도달 불가능한 예측 위치는 필터링되므로, 이 테스트를 통해 예측 가능 영역을 최대화하는 것이 중요합니다.

![Reachability.gif](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/Reachability.gif)

### 렌더링(Rendering)
렌더링 툴바를 사용하면 뷰에 표시되는 오브젝트의 투명도를 조절할 수 있습니다.
"collision mesh" 컨트로은 디버깅 용도로만 사용됩니다.

![RenderingToolbar.gif](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/RenderingToolbar.gif)

---
## 카메라(Cameras)

이 패널에서는 카메라 설정을 조정할 수 있습니다.

![camera panel.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/camera%20panel.png)

### Gain
- 카메라의 게인 값(비율)을 조정합니다.
- 최대 게인 값은 사용 중인 카메라 모델에 따라 다릅니다.
- 카메라가 지원하는 값보다 더 큰 게인을 설정하면, 자동으로 최대 허용 값으로 설정됩니다.
- 99로 설정하면 카메라가 지원하는 최대 게인 값이 적용됩니다.
### Exposure Mode (노출 모드)
- 수동과 자동 노출 모드 전환이 가능합니다.
- 자동 모드에서는 아래 슬라이더로 지정한 목표 밝기에 맞추어 카메라 노출이 자동으로 조정됩니다.
- 수동 모드에서는 노출 시간을 밀리초(ms) 단위 고정값으로 설정할 수 있습니다.

### Target Brightness(목표 밝기)
- 이미지의 목표 밝기 값을 설정합니다.
- "Live Images" 를 활성화하면 결과를 실시간으로 확인할 수 있습니다.

### Tolerance(허용 오차)
- 선택한 밝기 값의 대한 허용 오차를 설정합니다.
- 값이 낮을수록 카메라 노출이 더 자주 조정됩니다.

### Max Iterations(최대 반복 횟수)
- 목표 밝기를 달성하기 위해 카메라 소프트웨어가 이미지를 반환하기 전 반복할 최대 횟수를 설정합니다.

### Max Exposure(최대 노출)
- 카메라의 최대 노출 시간을 설정합니다.

### Select / Open File(파일 선택 / 열기)
- 캘리브레이션 절차가 완료되면 관련 캘리브레이션 파일(.rig)이 선택됩니다.
- "Open File"옵션을 통해 값을 확인할 수 있습니다.
### Locate Grid(그리드 찾기)
- 그리드(캘리브레이션 판)를 찾아 3D 환경에 그리드 오브젝트를 생성합니다.
- 그리드가 잘 보이고 자세가 올바르게 인식되는지 확인할 때 사용할 수 있습니다.

### Munaul Calibration(수동 캘리브레이션)
- 지정한 폴더에서 카메라 캘리브레이션 절차를 실행하고, 적절한 설정 파일을 생성합니다.
- 수동 캘리브레이션을 실행하면, 생성된 캘리브레이션 파일이 자동으로 선택되지 않습니다.
- 새 파일은 Rig Parameters 드롭다운에서 선택할 수 있습니다.

---

## AI Model(AI 모델)

이 패널은 AI 모델 및 관련 데이터를 선택, 로드, 검토하고, 로봇의 Grasp Point와 충돌 형상(Collision)을 정의하는 데 사용됩니다.
또한, 모델과 관련된 여러 설정을 지정하거나 디버깅 절차를 실행할 수도 있습니다.

선택한 모델 유형에 따라 UI에서 제공되는 옵션이 달라집니다.

Cambrian VISION 2.0에서는 두 가지 모델 유형을 지원합니다. 
- Standard Pose models : Pick Editor를 사용해 학습 전에 Grasp Point를 정의한 모델입니다.
- Full Pose models :  Cambrian UI에서 설정하며, 학습이 완료된 후 런타임에 Grasp Point를 정의 합니다. 이를 통해 런타인 중에도 Grasp Point와 해당 Collision Box를 자유롭게 변경할 수 있습니다.

### Model settings(모델 설정)
메인 AI 모델 패널에서는 AI 모델을 선택하고, 해당 모델의 다양한 설정을 조정할 수 있습니다.
모델이 로드되면 grasp point를 확인하거나 편집할 수 있습니다.

![AI models.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/AI%20models.png)

주요 기능 및 설정 항목
- Select Model 
	- 컴퓨터에 설치된 모든 모델을 목록으로 보여주며, 선택한 모델을 로드합니다.

- Name 
	- 현재 로드된 모델의 이름 표시합니다.

- Unload Model 
	- 현재 로드된 AI 모델을 언로드합니다.

- Open Folder
	- AI 모델이 저장된 폴더(`~/Desktop/Caint/Networks/<AI-Model>`)를 파일 탐색기로 엽니다.

- View / Edit Grasp Points
	- 모델의 그랩 포인트를 확인하거나 편집하는 모드로 전환합니다.

- Confidence Threshold
	- 예측을 유효하다고 판단하는 데 필요한 신뢰도(confidence) 값을 표시/설정합니다.
	- 범위 : 0~1, 일반적으로 0.9가 안전한 값입니다. 더 낮게 설정하면 예기치 않은 결과가 나올 수 있습니다.

- Visibility Threshold
	- 예측을 유효하다고 판단하는 데 필요한 가시성(visibility) 값을 표시/설정합니다.
	- 최소값은 모델에 지정, 최대값은 1, 일반적으로 0.9가 안전한 값입니다.

- Depth Centre
	- 현재 모델이 학습된 이상적인 작업 거리(깊이)를 표시합니다.

- Depth Range
	- 현재 모델이 학습된 이상적인 작업 거리의 범위를 표시합니다.
	- Depth Centre ± Depth Range 내에 있는 객체에 대해 최적의 성능을 보입니다.

- Max Tilt
	- 모델이 학습된 Pick 동작에서 허용되는 최대 틸트(카메라 시야방향(Z축) 기준, X,Y축 회전)를 표시합니다.

- Max Gamma
	- 모델이 학습된 Pick 동작에서 허용되는 Z축 회전의 최대값을 표시합니다.

- FOV%
	- 모델이 학습된 시야각(Field of View,FOV) 비율을 표시합니다.
	- 일부 모델은 작은 부품의 정확도를 높이기 위해 더 좁은 FOV로 학습됩니다.

- Resolution
	- 모델이 사용하는 이미지 해상도를 표시합니다.

- Model Type
	- 모델이 Full Pose인지 Standard Pose인지 표시합니다.

- Trim Image Edges
	- 이 값을 조정하면 이미지 가장자리에서 너무 가까운 위치의 Pick을 AI 모델이 무시하도록 할 수 있습니다.
	- 예를 들어 0.1로 설정하면, 이미지 가장자리 10% 이내에 있는 객체는 모두 무시됩니다.

- Recenter crops
	- 카메라의 스테레오 간격 변화 등을 보정할 수 있습니다.
	- 카메라에 변화가 생겼을 때 모델 재학습 없이도 보정 시도에 사용할 수 있습니다.

- Sorting Method
	- AI 모델이 반환하는 예측 결과의 정렬 기준을 설정합니다.
	- 로봇 명령(GET PREDICTION, GET ALL PREDICTIONS)에서 별도로 지정하면 이 설정을 덮어씁니다.

- GPU & CPU
	- 선택한 모델을 GPU 또는 CPU에 로드할지 선택할 수 있습니다.
	- GPU에 로드하면 연산 속도가 더 빠르지만, 동시에 로드할 수 있는 모델 수에는 제한이 있습니다.
	- 이 한도를 초과하면 Cambrian Vision UI에서 오류 메세지가 표시됩니다.

- Unlad All Models
	- 현재 Cambrian PC에 로드된 모든 AI 모델을 언로드합니다.

---

### Grasp Point View(그랩 포인트 뷰)

그랩 포인트 뷰는 정의된 그랩 포인트와 함께 부품을 표시합니다.
특정 그랩 포인트를 설정하면 해당 출동 형상 데이터도 확인 할 수 있습니다.
**Standard Pose**모델이 로드된 경우, 이 화면은 읽기 전용으로만 제공됩니다.

![6개의 서로 다른 그랩 포인트로 학습된 모델 예시.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/6%EA%B0%9C%EC%9D%98%20%EC%84%9C%EB%A1%9C%20%EB%8B%A4%EB%A5%B8%20%EA%B7%B8%EB%9E%A9%20%ED%8F%AC%EC%9D%B8%ED%8A%B8%EB%A1%9C%20%ED%95%99%EC%8A%B5%EB%90%9C%20%EB%AA%A8%EB%8D%B8%20%EC%98%88%EC%8B%9C.png)

주요 설명
- 위 예시 모델은 6개의 독립적인 그랩 포인트로 학습되었으며, 각각 고유한 ID가 할당됩니다.
- 로봇 API에서 특정 그랩 유형을 요청할 때는 이 ID를 참조합니다.
- **Grasp ID 0과 5(G8 및 G11)** 는 동일한 위치에 정의되었지만 방향이 서로 반대입니다.
	- 이는 부품을 집을 때 로봇이 90도 이상 회전하는 것을 방지하기 위한 일반적인 설계 방식입니다.

### Creating/Editing a Grasp Point(그랩 포인트 생성/편집)
"Full Pose"모델에서는 그리퍼의 그랩 포인트와  Collision Box를 런타임으로 정의할 수 있습니다.
"Add Grasp Point"버튼을 사용해 새로운 그랩 포인트를 추가할 수 있습니다.
추가된 후에는 에디터에서 값을 직접 입력하거나, 기즈모를 이용해 위치와 방향(이동 및 회전)을 조정할 수 있습니다.

![grasp points.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/grasp%20points.png)

### Grasp Point Editor(그랩 포인트 에디터)
- Name(String)
	- 그랩 포인트의 이름을 입력합니다.

- ID(Integer)
	- 각 그랩 포인트에는 고유한 ID가 할당되어야 합니다.
	- 이 ID는 로봇 API와 통신할 때 사용되며, 다양한 로봇 동작을 트리거하는 데 활용할 수 있습니다.

- TX/TY/TZ(Real number, mm)
	- 그랩 위치의 중심 좌표를 의미합니다.
	- 그랩 포인트는 부품의 원점 기준으로 정의됩니다.

- RX/RY/RZ(Real number, degrees)
	- 각 축을 기준으로 한 그랩 포인트의 회전 각도입니다.

- Rotational Symmetry(Logical - true/false)
	- 이 옵션을 키면 그랩 포인트가 중심점을 기준으로 대칭임을 정의합니다.

- Cylindrical(Logical - true/false)
	- 이 옵션을 키면 오프셋이 있는 축을 기준으로 회전 대칭을 갖는 그랩 포인트를 정의합니다.

- Rotational Center(회전 중심)
	- TX/TY/TZ(Real number, mm)
		- 회전 축의 원점 좌표입니다.
	- RX/RY(Real number, degrees)
		- 회전 축의 각도입니다.
	- Rotation Range(Real number, degrees)
		- 해당 축을 기준으로 회전할 수 있는 범위를 제한 합니다.

---

### Collision Box editor(충돌 박스 에디터)
그랩 포인트를 선택하면, 해당 그랩 포인트에 연결된 충돌 박스의  형상을 편집할 수 있습니다.
하나의 그랩 포인트에 여러 개의 충돌 박스를 생성하는 것도 가능합니다.

충돌 박스는 에디터에서 직접 값을 입력하거나, 기즈모를 사용해 위치 이동 및 크기 조절로 편집할 수 있습니다.
- TX/TY/TZ(Real number, mm)
	- 충돌 박스 중심점의 좌표입니다.

- RX/RY/RZ(Real number, degrees)
	- 각 축을 기준으로 한 충돌 박스의 회전 각도입니다.

- SX/SY(Real number, mm)
	- 충돌 박스의 크기(가로, 세로)입니다.
	- 충돌 박스의 길이(로봇 TCP와 그랩 포인트 사이를 잇는 부분)는 조정할 수 없습니다.

![collision box.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/collision%20box.png)

---
### Tool Box(툴 박스)

툴 박스는 그랩 포인와 충돌 박스를 설정/편집하는 데 도움이 되는 추가 옵션을 제공합니다.

![Toolbox.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/Toolbox.png)

주요기능
- Undo/Redo(실행 취소/다시실행)
	- 그랩 포인트 또는 충돌 박스 데이터에 대한 모든 편집 작업에 적용됩니다.

- Duplicate(복제)
	- 현재 선택된 그랩 포인트 또는 충돌 박스를 복제합니다.

- Flip(뒤집기)
	- 현재 그랩 포인트의 방향을 반대로 전환합니다.

- Interactive Edit(인터랙티브 편집)
	- 편집 모드를 변경하여, 그랩 포인트를 형상에 맞춰 동적으로 이동시킬 수 있습니다.
	- Escape 키로 취소, 마우스 왼쪽 클릭 또는 Enter 키로 확정할 수 있습니다.

- XYZ 버튼
	- 그랩 포인트 또는 충돌 박스의 바향을 고정된 각도만큼 변경합니다.
	- 각도 중분은 슬라이더나 값 입력으로 조정할 수 있습니다.

---
### Prediction Window(예측 창)
예측이 수행될 때마다 아래와 같이 인터페이스에 예측 창이 열립니다.
이 데이터는 사용자가 어떤 예측이 중요한지, 그리고 특정 예측이 왜 우선순위가 되었는지 해석하는 데 도움을 줍니다.

![prediction window.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/prediction%20window.png)

왼쪽 창의 파라미터 해석
- ID(int) : 이미지에서 네모 박스와의 대응 관계를 나타냅니다.
- CONF(float) : 신뢰도(Confidence) 값으로, 0 ~1.0 사이 값입니다.
- VIS(float) : 가시성(Visibility) 값으로, 0 ~ 1.0 사이의 값입니다.(지원되는 모델에서만 표시)
- OBJ(int) : 다중 부품 모델에서 객체 ID를 나타냅니다. 단일 부품 모델의 경우 항상 0입니다.
- GRASP(int) : 그랩 포인트에 대해 정의된 그룹 ID와 대응합니다.
- RX°(float) : X축(좌우 축, 카메라 이미지 기준) 주위의 "Alpha" 회전 각도
- RY°(float) : Y축(상하 축, 카메라 이미지 기준) 주위의 "Beta" 회전 각도
- RZ°(float) : Z축(이미지 안쪽 방향) 주위의 "Gamma" 회전 각도
>[!tip] 참고
>Alpha, Beta, Gamma는 오일러 각이며, 회전 순서는 ZXY입니다.
>부품의 x-y 값은 네모 박스의 중심 좌표이며, 시스템은 이를 로봇 월드의 x,y좌표로 변환합니다.

카메라 오버레이(오른쪽 이미지)
- 오른쪽 카메라 오버레이에 표시되는 숫자는 예측 창의 각 항목과 일치합니다.
- 오른쪽 상단의 오버레이 체크박스를 통해 색깔 표시 여부를 전환할 수 있습니다.

---
### Prediction Overlap(예측 오버랩)
예측된 부품들은 예측 결과의 특성을 나타내기 위해 다양한 색상으로 표시됩니다.

![green.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/green.png)

- 초록색
	- 가장 높은 신뢰도(Confidence)룰 가진 예측 부품을 나타냅니다.
	- 이 예측은 로봇 API로 전달되어 실제로 집기 동작에 사용됩니다.

![blue.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/blue.png)

- 파란색
	- 남아있는(선택되지 않은) 예측 부품들을 나타냅니다.

![yellow.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/yellow.png)

- 노란색
	- AI 모델의 예측 범위를 벗어난(너무 가깝거나, 너무 먼) 부품을 나타냅니다.

![red.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/red.png)

- 빨간색
	- 집을 경우 충돌이 발생할 것으로 예상되는 부품을 나타냅니다.

![orange.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/orange.png)

- 주황색
	- 사용자가 설정한 가시성(Visibility) 또는 신뢰도(Confidence) 임계값에 의해 필터링된 부품을 나타냅니다.

![purple.png](/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/purple.png)

- 보라색
	- 그랩 포인트가 다른 부품에 의해 가려져 있거나 , 접근이 불가능한(예 : 부품의 아랫면에 위치한) 경우를 나타냅니다.

---
## Log(로그)
디버그 로그의 표시를 켜거나 끌 수 있습니다.

## Hot keys(단축키)
Cambrian Vision UI에서 자주 사용하는 작업을 빠르게 수행할 수 있는 단축키 입니다.

| 일반          | F11      | 전체 화면 모드 전환          |
| ----------- | -------- | -------------------- |
|             | Esc      | 팝업 창 닫기              |
| 그랩 포인트      | Ctrl + s | 변경 사항 저장             |
|             | Ctrl + d | 그랩 포인트 복제            |
|             | Ctrl + g | 새 그랩 포인트 생성          |
|             | Del      | 그랩 포인트 삭제            |
|             | Tab      | 에디터 내 필드 간 이도        |
|             | Space    | 필드 활성화(체크박스, 드롭다운 등) |
| 인터랙티브 편집 모드 | Esc      | 인터랙티브 편집 취소          |

---

# Demonstration Videos(데모 영상)

<video controls width="100%"> <source src="/img/user/files/%EC%BA%A0%EB%B8%8C%EB%A6%AC%EC%95%88%20UI%20%EB%A9%94%EB%89%B4%EC%96%BC/Fullpose_demo.mp4" type="video/mp4"> 죄송합니다. 귀하의 브라우저는 비디오 태그를 지원하지 않습니다. </video>
---
# Updating the Cambrian VISION Software(소프트웨어 업데이트)

Cambrian VISION의 새로운 버전은 [Software Downlads](https://documentation.cambrianrobotics.ai/en/cambrian-vision-system/latest/software-downloads) 페이지에서 다운로드할 수 있습니다.

다운로드한 파일은 Cambrian PC의 `~/Download` 폴더에서 복사해야 합니다.
또는, 다른 PC에서 USB 드라이브를 이용해 파일을 옮길 수도 있습니다.
해당 파일을 더블 클릭하면 설치가 진행됩니다.
