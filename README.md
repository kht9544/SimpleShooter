# 🎯 Simple Shooter - 언리얼 엔진 4 FPS 게임

**Simple Shooter**는 **Unreal Engine 4.2**로 개발된 **1인칭 슈팅 게임(FPS)**입니다.  
AI 적들과 전투하며, 다양한 무기를 사용해 승리를 목표로 하는 게임입니다.

---

## 🛠️ 프로젝트 목적

- **언리얼 엔진**
- **C++**
- **Behavior Tree & Blackboard** (AI 시스템)
- **UE5 내장 UI 시스템** (HUD, 위젯)
- **Physics & Collision System** (총기 물리 효과)

## 📌 주요 기능

### 🔫 전투 시스템
- **무기 시스템**: 총기 발사, 탄환 충돌 판정 및 데미지 처리 구현 (`Gun.cpp`)
- **플레이어 공격**: 무기 발사 시 이펙트 및 사운드 효과 추가
- **AI 공격**: AI가 특정 조건에서 플레이어를 인식하고 공격 (`BTTask_Shoot.cpp`)

### 🧠 AI 시스템
- **AI 행동 트리**를 활용한 적 캐릭터의 행동 결정 (`ShooterAIController.cpp`)
- **플레이어 감지 서비스** (`BTService_PlayerLocationIfSeen.cpp`): AI가 플레이어를 시야에서 포착할 경우 행동 변경
- **블랙보드 값 초기화** (`BTTask_ClearBlackboardValue.cpp`): 특정 조건에서 블랙보드 값 리셋

### 🎮 플레이어 시스템
- **이동 및 조작 시스템** (`SimpleShooterCharacter.cpp`)
  - 이동, 점프, 시점 회전, 공격 기능
- **UI 시스템** (`ShooterPlayerController.cpp`)
  - HUD, 승리 및 패배 화면 표시
- **체력 시스템** (`ShooterCharacter.cpp`)
  - 피해를 입을 경우 체력 감소, 사망 시 게임 종료 처리

### 🏆 게임 모드 시스템
- **일반 게임 모드** (`SimpleShooterGameMode.cpp`)
  - 기본 게임 흐름 제어
- **킬 엠 올 모드** (`KillEmAllGameMode.cpp`)
  - 모든 AI 적을 처치하면 승리, 플레이어가 사망하면 패배 처리

---

## 🎮 게임 플레이

1️⃣ **적 AI가 플레이어를 감지**하면 공격을 시작합니다.  
2️⃣ 플레이어는 **총기를 발사하여 적을 처치**해야 합니다.  
3️⃣ **모든 적을 제거하면 승리**하며, 플레이어가 사망하면 패배합니다.  

---

## 🎯 프로젝트를 통해 배운 점 📖

1. **언리얼 엔진의 AI 시스템 이해**
   - `Behavior Tree`와 `Blackboard`를 사용하여 AI를 제어하는 방법을 익혔다.
   - AI의 감지, 추적, 공격 로직을 구현하면서 AI 개발에 대한 이해도를 높일 수 있었다.

2. **객체 지향 프로그래밍(OOP)과 설계 원칙 학습**
   - `Gun` 클래스와 `ShooterCharacter` 클래스를 분리하여 모듈화하고, 유지보수성을 높였다.
   - 캡슐화 및 상속을 활용하여 확장 가능한 구조를 설계하는 법을 배웠다.

3. **디버깅 및 문제 해결 능력 향상**
   - AI가 정상적으로 동작하지 않을 때 `UE_LOG`를 활용한 디버깅 방법을 익혔다.
   - `Breakpoints`를 활용하여 코드의 흐름을 추적하고 버그를 해결하는 능력을 키웠다.

4. **UI 시스템 활용 경험**
   - `HUD` 및 `게임 종료 화면`을 위젯으로 구현하여 UI 시스템을 효율적으로 다루는 방법을 배웠다.


