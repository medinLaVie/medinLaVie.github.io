---
title:  "Prettify Json"
date:   2024-04-11 9:00:00 # 4/3 10:20-
layout: page
#
# toc: true
# categories:
---

```python
import json

res = {'news': [{'title': 'Rotary Pendulum RL', 'description': 'Open Source project aimed at controlling a real life rotary pendulum using RL algorithms'}, {'title': 'DQN Implementation from scratch', 'description': 'Developed a Deep Q-Network algorithm to train a simple and double pendulum'}, {'title': 'Multi Agents HAED', 'description': 'University project which focuses on simulating a multi-agent system to perform environment mapping. Agents, equipped with sensors, explore and record their surroundings, considering uncertainties in their readings.'}, {'title': 'Wireless ESC for Modular Drones', 'description': 'Modular drone architecture proposal and proof of concept. The project received maximum grade.'}]}

print(json.dumps(res, indent=2))
```

https://github.com/VinciGit00
