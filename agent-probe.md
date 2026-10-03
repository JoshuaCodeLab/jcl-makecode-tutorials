# JCL Agent Probe

### @explicitHints true

## Step 1

채팅에 **probe**를 입력했을 때 코드가 실행되도록 준비해 봅시다. 시작 블록의 명령 이름을 확인하세요. Agent가 할 일은 어느 블록 안에 넣어야 할까요? 먼저 생각해 보고, 도움이 필요하면 전구를 누르세요.

### ~ tutorialhint

``||player:on chat command||`` 블록 안에 Agent가 할 일을 넣습니다. 명령 이름은 **probe**로 맞춥니다.

```blocks
player.onChat("probe", function () {
})
```

## Step 2

Agent를 플레이어에게 데려온 뒤 앞으로 한 칸 이동시켜 보세요. 두 동작은 어떤 순서여야 할까요? 먼저 블록을 조립한 다음 **Play**를 누르고 Minecraft 채팅에 **probe**를 입력해 확인하세요. 도움이 필요하면 전구를 누르세요.

### ~ tutorialhint

``||agent:agent teleport to player||`` 다음에 ``||agent:agent move||``를 넣습니다. 이동 방향은 **forward**, 거리는 **1**입니다.

```blocks
player.onChat("probe", function () {
    agent.teleportToPlayer()
    agent.move(FORWARD, 1)
})
```

## Step 3

이번에는 Agent가 플레이어에게 돌아온 뒤 앞으로 세 칸 이동하게 바꿔 보세요. 어느 값을 바꾸면 될까요? 먼저 수정하고 **Play**를 누른 뒤 채팅에 **probe**를 입력해 확인하세요. 도움이 필요하면 전구를 누르세요.

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
