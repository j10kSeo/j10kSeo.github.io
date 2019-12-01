---
title: "My Custom Settings For Intellij"
date: 2019-12-01
categories: productivity, Intellij
---


Intellij IDEA의 default 설정으로는 부족하거나 불편한 부분이 있다.

아래 customizing이 여러모로 편리하여 기록해둔다.

# Keymaps

## Nav

- Declaration
  - ⌘B :arrow_right: ⌘↑
  - (⌘↑는 `Jump to Navigation Bar`가 기본인데 거의 사용하지 않는다. 일단은 ⌘B로 바꾸어 놓았으나 사용한 적은 없다.)
  - Jump to Source가 ⌘↓라서 JS에서 코드 이동할 때 상반되는 동작을 한다. 따라서 상하 키로 변환하면 직관적이다.
  
- SmartType
  - Add ⌘M
  - (⌘M은 `Window - minimize`가 기본인데 한 번도 사용한 적이 없어 제거하였다.)
  - SmartType은 원래 ⌃⇧Space로 매핑되어 있는데 새끼손가락이 아프다. 
    
- Anything related with reformating
  - Use ⌘L
    - 이건 개인적인 용도에 맞춰서, 대신 L이 reformating에 많이 쓰이는 문자이므로 활용도에 맞춰 사용하면 되겠다. `Plug-ins - JavaScrpit - Fix EsLint Problems`를 자주 사용하기 때문에 이로 매핑해서 사용중이다.
  - (⌘L은 `Navigate - Line/Column` 이 기본인데 사용할 일이 거의 없다. ⌘는 명령을 실행하는 느낌이고, ⇧⌘는 advanced-command 의 느낌이 강하다. ⇧⌘L으로 승격시켜 주었다.)

- Auto-Indent Lines
  - ⌃⌥I :arrow_right: ⌘I
  - (⌘I는 Plug-ins - Database&SQL 의 Data Source Properties로 매핑되어 있다. 겹칠 일이 적어서 그냥 놔둔다.)
  - ⌃⌥ 은 누르기가 힘들어 차라리 단축키가 없는 편이 낫다고 생각한다.
  
- Increase/Decrease Font Size
  - Use ⌥=, ⌥- (+, -)
  - 요새 눈이 침침하여 자주 사용한다.

# Live Templates

- console.log
  - Abbreviation: cc
  - Template text: `console.log("[JONGMAN_LOG] $VAR$", $VAR$, new Date(Date.now() - new Date().getTimezoneOffset() * 60000).toISOString().split('T')[1].slice(0, -1));`
  - 뒤의 new Date 이하는 HH:mm:ss.fff 를 현지 시각 기준으로 표현하기 위한 용도이다.