# Progression Tracking

Use this file when the user is learning a topic across multiple sessions or wants a study plan.

## Track Four Dimensions

For each topic, quickly estimate:
- **Orientation**: can the user place the topic in the bigger system?
- **Explanation**: can the user explain it in plain language?
- **Operation**: can the user use it in practice?
- **Diagnosis**: can the user debug common failures?

Use three simple levels:
- `0` unfamiliar
- `1` partial / guided
- `2` independent

## Fast Assessment Prompts

Use one short prompt per dimension when needed:
- Orientation: "这东西在整套系统里是干嘛的？"
- Explanation: "你用自己的话讲一下它是什么。"
- Operation: "真到机器上，你会先做哪一步？"
- Diagnosis: "如果它坏了，你先查什么？"

## Stage Model

Map the user to one stage:
- **Stage 1 认路**: knows the names, lacks flow
- **Stage 2 能讲**: can explain the basics
- **Stage 3 能做**: can complete common tasks
- **Stage 4 能排障**: can debug routine issues
- **Stage 5 能迁移**: can apply the idea to adjacent problems

## What To Do Next

- If Orientation is weak: teach map before details
- If Explanation is weak: simplify the mental model and compare nearby concepts
- If Operation is weak: use a mini workflow or command path
- If Diagnosis is weak: teach symptom-first troubleshooting

## Progress Update Format

Use a compact status when useful:
- `Topic`: [name]
- `Stage`: [1-5]
- `Strength`: [best dimension]
- `Gap`: [weakest dimension]
- `Next`: [one concrete lesson target]
