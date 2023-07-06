---
id: jd5f4c9izgu4aq76f3z4fkj
title: Daily
desc: ''
updated: 1688561659503
created: 1688552042623
status: 'w'
priority: '4'
owner: 'dwl'
TODO: ''
---

<!--
- inherit todo-elements not done in hierarchy
- scoping
-->

```handlebar
Handlebars.registerPartial(
  "task",
  "{{task.element}}
)
```

{{#each tasks}}
  {{>task task=.}}
{{/each}}

## daily
{{log}}