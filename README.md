<img src="https://capsule-render.vercel.app/api?type=waving&color=0:cd93a5,10:ddb6c2,25:edd9df,45:c7e5dc,65:b6ddd1,80:d3e6ea,100:b6d6dd&height=200&section=header&text=Hello!&fontColor=f7fafb&fontSize=50&fontAlignY=35&animation=twinkling" width="100%"/>

![alt text](https://img.shields.io/badge/SQL-d8ede7)
![alt text](https://img.shields.io/badge/Git-ddefea)
![alt text](https://img.shields.io/badge/Jira-c7e5dc)
![alt text](https://img.shields.io/badge/Confluence-b6ddd1)
![alt text](https://img.shields.io/badge/Figma-b3cec6)

![alt text](https://img.shields.io/badge/MarkDown-d8ede7)
![alt text](https://img.shields.io/badge/Python-ddefea)

![alt text](https://img.shields.io/badge/SOMSAMTAM-d8ede7)
![alt text](https://img.shields.io/badge/GoodUI-ddefea)
![alt text](https://img.shields.io/badge/FlyWheel-c7e5dc)


name: generate animation
on:
  schedule:
    - cron: "0 */24 * * *" 
  workflow_dispatch:
  push:
    branches:
    - master
    
jobs:
  generate:
    permissions: 
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5
    
    steps:
      # generates a snake game from a github user (<github_user_name>) contributions graph, output a svg animation at <svg_out_path>
      - name: generate github-contribution-grid-snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: 여기다가 github ID 적기 !!!
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark

      - name: push github-contribution-grid-snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

[Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FJunTaeHahm&count_bg=%230C1117&title_bg=%230C1117&icon=cloudsmith.svg&icon_color=%23FFFFFF&title=Hello%21&edge_flat=false)](https://hits.seeyoufarm.com)

<details>
<summary>더보기</summary>
블라블라
</summary>
</details>


<img src="https://capsule-render.vercel.app/api?type=rect&color=0:d8ede7,20:e9f5f2,40:d8e9ed,60:e9f3f5,80:d8e9ed,100:c7dfe5&height=40&section=footer&text=&fontSize=0" width="100%"/>

