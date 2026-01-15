```mermaid
flowchart TD
    C["t-1"]
    A["x（HD用户）<br/>用户衰减参数α"]
    D["0（Locker用户）<br/>用户衰减参数δ"]
    B["1-x（非HD/Locker用户）<br/>用户衰减参数β"]

    C-->H["t"]

    A -->|剩余市场份额| E["(1-α)x<br/>HD用户"]
    A -->|用户流失| F["αx+β(1-x)<br/>Locker用户"]

    B -->|广告/口碑进入Locker| F
    B -->|剩余市场份额| G["(1-β)(1-x)<br/>非HD/Locker用户"]

    D -->F

    H -->I["t+1"]
    E -->|剩余市场份额| J["[(1-α)^2]x<br/>HD用户"]
    E -->|用户流失| K["α(1-α)x+[αx+β(1-x)]+β(1-β)(1-x)<br/>Locker用户"]

    F -->|剩余市场份额| K
    F -->|用户流失| L["[(1-β)^2](1-x)+δ[αx+β(1-x)]<br/>非HD/Locker用户"]

    G-->|广告/口碑进入Locker| K
    G -->|剩余市场份额| L["[(1-β)^2](1-x)<br/>非HD/Locker用户"]









