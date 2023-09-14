---
title: "quartz"
tags:
- "dev-logs"
---

Log what I have done to use quartz as my new site.

1. Forked the repo [jackyzha0/quartz: 🌱 host your own second brain and digital garden for free (github.com)](https://github.com/jackyzha0/quartz)
2. Renamed it to gr-grey.github.io
3. Deploy it by allowing read and write permission, and set github page publish (though not sure if necessary since the github.io name change) [Deploying Quartz to the Web (jzhao.xyz)](https://quartz.jzhao.xyz/notes/hosting/).
4. Configure: change baseURL in "config.toml" and cname in ".github/workflows/deploy.yaml"
5. push changes `git push origin hugo`