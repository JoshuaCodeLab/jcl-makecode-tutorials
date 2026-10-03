# JCL Agent Probe

### @explicitHints true
### @hideDone true

## Step 1

채팅에 **probe**를 입력했을 때 코드가 실행되도록 준비해 봅시다. 시작 블록의 명령 이름을 확인하세요. Agent가 할 일은 어느 블록 안에 넣어야 할까요? 먼저 생각해 보고, 도움이 필요하면 전구를 누르세요.

### ~ tutorialhint

``||player:on chat command||`` 블록 안에 Agent가 할 일을 넣습니다. 명령 이름은 **probe**로 맞춥니다.

```blocks
player.onChat("probe", function () {
})
```

## Step 2

Agent가 플레이어에게 온 뒤 앞으로 1칸 이동하게 만드세요. 두 동작의 순서를 먼저 생각해 조립하세요. 필요하면 전구를 누르세요.

**실행:** **Play** → 채팅에 **probe** → 돌아오기와 **1칸 이동** 확인.

**확인한 뒤에만 C로 돌아와 Next를 누르세요.**

### ~ tutorialhint

``||agent:agent teleport to player||`` 다음에 ``||agent:agent move||``를 넣습니다. 이동 방향은 **forward**, 거리는 **1**입니다.

```blocks
player.onChat("probe", function () {
    agent.teleportToPlayer()
    agent.move(FORWARD, 1)
})
```

## Step 3

어느 숫자를 바꾸면 3칸 이동할까요? 다른 블록은 그대로 두고 **1 → 3**만 바꾸세요. 필요하면 전구를 누르세요.

**비교:** **Play** → 채팅에 **probe** → 플레이어에게 돌아온 뒤 **3칸 이동** 확인. 1칸일 때와 비교하세요.

확인하면 활동 완료! **C**로 코드를 다시 보고, **Esc**로 Code Builder를 닫으세요.

### ~ tutorialhint

``||agent:agent move||``의 이동 거리를 **1 → 3**으로 바꿉니다.

```blocks
player.onChat("probe", function () {
    agent.teleportToPlayer()
    agent.move(FORWARD, 3)
})
```

```template
player.onChat("probe", function () {
})
```
