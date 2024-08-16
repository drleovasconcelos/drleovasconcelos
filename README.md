![image](https://github.com/drleovasconcelos/drleovasconcelos/assets/111660177/be4fb370-ea64-43ab-82ba-da3e55926ffe)

## Oiii eu sou a Leonardo Freire, programador Full Stack e Apaixonado por Tecnologia!

Atualmente atuo em uma posição de gestão no Centro Universitário Estácio do Ceará, mas minha verdadeira paixão é a tecnologia. Ao longo dos anos, venho me dedicando a aprender e explorar cada vez mais este universo fascinante.

🌱 Aprendizado Contínuo: Estou continuamente me aperfeiçoando em Análise de Dados e Desenvolvimento Full Stack, o que me permite transformar dados em insights valiosos e construir soluções tecnológicas robustas e eficientes.

🚀 Transição de Carreira: Minha trajetória combina habilidades em liderança e gestão com uma sólida formação em tecnologia, resultando em uma perspectiva única para resolver problemas complexos e liderar equipes em ambientes dinâmicos.

🔍 Projetos e Colaborações: Aqui no GitHub, você encontrará uma coleção dos meus projetos mais recentes, onde aplico meu conhecimento em programação, análise de dados e desenvolvimento web. Cada projeto é uma oportunidade para crescer e contribuir com soluções inovadoras.

💡 Objetivo: Estou em busca de novas oportunidades para aplicar e expandir meu conhecimento técnico, especialmente em áreas que envolvem análise de dados, desenvolvimento web e liderança de projetos.

<!--icondev.dev-->

<div style="text-align: center">
  <img height="150cm" src="https://github-readme-stats.vercel.app/api?username=drleovasconcelos&theme=vue-dark&show_icons=true&hide_border=false&count_private=true"/>
  <img height="150cm" src="https://github-readme-stats.vercel.app/api/top-langs/?username=drleovasconcelos&theme=vue-dark&show_icons=true&hide_border=false&layout=compact"/>
</div>

<div style="display: inline_block"><br>
  <img align="center" alt="Rafa-Js" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-plain.svg">
  <img align="center" alt="Rafa-Ts" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-plain.svg">
  <img align="center" alt="Rafa-React" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg">
  <img align="center" alt="Rafa-HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
  <img align="center" alt="Rafa-CSS" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
  <img align="center" alt="Rafa-Python" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
  <img align="center" alt="Rafa-Csharp" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/csharp/csharp-original.svg">
</div>
  
  ##

 <!--dev.to-->
<div> 
  <a href="#" target="_blank"><img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" target="_blank"></a>
  <a href="https://www.instagram.com/dr.leovasconcelos" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
 	<a href="#" target="_blank"><img src="https://img.shields.io/badge/Twitch-9146FF?style=for-the-badge&logo=twitch&logoColor=white" target="_blank"></a>
 <a href="https://discord.com/channels/@leonardofreire_" target="_blank"><img src="https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white" target="_blank"></a> 
  <a href = "lfreire1985@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
  <a href="https://www.linkedin.com/in/leonardofv" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
  
</div>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/YourUser/drleovasconcelos/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/YourUser/drleovasconcelos/output/github-contribution-grid-snake.svg">
  <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/YourUser/drleovasconcelos/output/github-contribution-grid-snake.svg">
</picture>

name: generate animation

on:
  # run automatically every 24 hours
  schedule:
    - cron: "0 */24 * * *" 
  
  # allows to manually run the job at any time
  workflow_dispatch:
  
  # run on every push on the master branch
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
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
          
          
      # push the content of <build_dir> to a branch
      # the content will be available at https://raw.githubusercontent.com/<github_user>/<repository>/<target_branch>/<file> , or as github page
      - name: push github-contribution-grid-snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          
<!--
**drleovasconcelos/drleovasconcelos** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 Atualmente estou trabalhando em cargo de Gestão no Centro Universitário Estácio do Ceará, no entanto sigo encantado com os conhecimentos que venho adquirindo na área da tecnologia.
- 🌱 Desta forma, atualmente estou estudando e me aprofundando em Análise de Dados e fazendo o curso de Full Stack. 
-->
