- 👋 Hi, I’m @rafaeloliveira
- 👀 I’m interested in become software Developer
- 🌱 I’m currently learning Python, HTML, CSS, JS 
- 💞️ I’m looking to collaborate on development
- 📫 How to reach me eurafaelmedeiros@gmail.com

<!---
rafaloliveira/rafaloliveira is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=rafaloliveira&layout=compact&show_icons=true&border_radius=10&theme=merko)](https://github.com/anuraghazra/github-readme-stats)



<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" width="50"/><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original-wordmark.svg" width="50" /><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" width="50"/><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original-wordmark.svg" width="50"/><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original-wordmark.svg" width="50"/>

![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=rafaloliveira&show_icons=true&border_radius=10&theme=merko)
name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: rafaloliveira
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
