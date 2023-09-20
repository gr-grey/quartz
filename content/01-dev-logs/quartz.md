---
title: "quartz"
tags:
- "dev-logs"
---

2023-09-14

Upgrade to quartz 4.0

 - save content somewhere else
 - fetch and sync to v4 branch (force, discard conflicts changes)
 - npm i, npx quartz create, Copy and existing folder, choose how links are resolved, pick shortest path (may need to update links later)
 - npx quartz build --serve
 - restore content/.gitkeep
 - git ignore dot obsidian 
 - add all, push to v4
 - edit quartz.config.ts, change site name and base_url
 - add .github/workflows/deploy.yml according to [Hosting (jzhao.xyz)](https://quartz.jzhao.xyz/hosting) page
 - add the  file, not commit
 - go to github repo, change default branch to v4
 - go to page -> source select github action
 - locally, run npx quartz sync, it commits the deploy.yml
 - it's served at gr-grey.github.io, not gr-grey.github.io\/repo name, maybe because base_url was set to be just gr-grey.github.io


Log what I have done to use quartz as my new site.

1. Forked the repo [jackyzha0/quartz: 🌱 host your own second brain and digital garden for free (github.com)](https://github.com/jackyzha0/quartz)
2. Renamed it to gr-grey.github.io
3. Deploy it by allowing read and write permission, and set github page publish (though not sure if necessary since the github.io name change) [Deploying Quartz to the Web (jzhao.xyz)](https://quartz.jzhao.xyz/notes/hosting/).
4. Configure: change baseURL in "config.toml" and cname in ".github/workflows/deploy.yaml"
5. push changes `git push origin hugo`