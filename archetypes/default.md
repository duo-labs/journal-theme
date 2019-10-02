---
title: "{{ replace (replace .Name "-" " ") "_" " " | title }}"
date: {{ .Date }}
draft: true
authors: ["{{getenv "USER"}}"]
---

