# Don't Sleep

🚀 **서울대학교 "소프트웨어 개발의 원리 및 실습 (M1522.002400)" 팀 프로젝트**

## 🎮 데모 플레이

게임은 [여기](https://dandyday.github.io/DontSleep/)에서 플레이하실 수 있습니다!

---

## 📌 프로젝트 개요

**Don't Sleep**은 **<8번 출구>류 게임**으로 불리는 **리미널 스페이스 장르**의 게임입니다. 게임에 대한 자세한 설명은 [게임 매뉴얼](Manual.md)에서 확인할 수 있습니다.

본 프로젝트에서 **PM**을 맡아 **프로젝트의 전반적인 진행을 관리**하였으며, 팀을 디자인 팀/코드 팀으로 나누고, 애자일 방법론을 적용하여 팀원들의 업무를 체계적으로 관리했습니다. 또한, **일부 기능의 리팩터링 및 구현을 직접 담당**하였습니다.

프로젝트의 자세한 진행 내역은 [Don't Sleep Wiki](https://github.com/2024FALL-SWPP/team-project-for-2024-fall-swpp-team-20/wiki)에서 확인할 수 있습니다.


---

## 🔧 구현에 참여한 핵심 기능

### 1️⃣ 인터랙션 관련 기능

플레이어는 방 안의 다양한 오브젝트와 상호작용할 수 있습니다. 이를 위해 **`IInteractable` 인터페이스**와 **`InteractableObject` 추상 클래스**를 설계 및 구현하였습니다.

🔹 **주요 구현 내용:**
- 플레이어의 **`InteractionHandler` 컴포넌트**가 각 오브젝트와 상호작용 가능하도록 설계
- **`InteractableObject` 클래스**를 통해 상호작용 가능한 오브젝트에 **테두리 이펙트 적용**
- **확장성을 고려한 구조 설계**로, 다양한 오브젝트에 쉽게 인터랙션 기능 추가 가능

📌 **결과:**
게임 내 상호작용 시스템이 직관적으로 개선되어 플레이어 경험 향상.

<div style="display: flex; justify-content: space-between;">
  <img src="https://github.com/user-attachments/assets/62125080-bf1a-4b5d-a792-068f0c81c3db" alt="인터랙션 이미지 (전)" style="width: 45%;"/>
  <img src="https://github.com/user-attachments/assets/b7016ce1-7f50-4ac0-adac-67b88a5c891e" alt="인터랙션 이미지 (후)" style="width: 45%;"/>
</div> 

---

### 2️⃣ 테스트 환경 자동화 구축

프로젝트의 PM으로서, 팀원들이 구현한 기능을 보다 안정적으로 개발할 수 있도록 **자동화된 테스트 환경**을 구축하였습니다.

🔹 **주요 구현 내용:**
- **Unity Test Framework**를 활용하여 기능별 테스트 코드 작성
- **Unity GameCI**를 도입하여 **CI/CD 환경 구축**
- **Pull Request 시 자동 테스트 실행**을 설정하여 `develop` 브랜치의 안정성 유지

📌 **결과:**
개발 중 기능 테스트의 일관성을 유지하고, 팀원들이 보다 효율적으로 개발 가능.

자세한 내용은 [테스트 문서](https://github.com/2024FALL-SWPP/team-project-for-2024-fall-swpp-team-20/wiki/Final-Testing)에서 확인할 수 있습니다.

---

### 3️⃣ 코드 리팩터링

수업에서 배운 내용을 바탕으로, 여러 가지 리팩터링 작업을 수행했습니다.

🔹 **주요 리팩터링 내용:**
- **디자인 패턴 적용** (싱글톤, 팩토리 패턴 등)
- **중복 코드 제거 및 모듈화**
- **코드 로직 최적화**를 통한 성능 개선

📌 **결과:**
코드의 가독성이 향상되고, 유지보수가 용이해짐.

자세한 내용은 [디자인 패턴 문서](https://github.com/2024FALL-SWPP/team-project-for-2024-fall-swpp-team-20/wiki/Final-Design-Patterns) 및 [리팩터링 문서](https://github.com/2024FALL-SWPP/team-project-for-2024-fall-swpp-team-20/wiki/Final-Refactoring)에서 확인할 수 있습니다.
