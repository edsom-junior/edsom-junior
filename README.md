<!--
  README de perfil — Edsom Junior
  Identidade visual: preto, azul e azul-claro
-->

<div align="center">

  <!-- BANNER -->
  <img
    src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:0A2A66,100:58A6FF&height=220&section=header&text=EDSOM%20JUNIOR&fontSize=42&fontColor=FFFFFF&fontAlignY=35&desc=Ci%C3%AAncia%20da%20Computa%C3%A7%C3%A3o%20%7C%20Desenvolvimento%20de%20Software&descSize=15&descAlignY=55&descColor=BBD7FF"
    width="100%"
    alt="Banner Edsom Junior"
  />

  <!-- ANIMAÇÃO DE TEXTO -->
  <img
    src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&duration=3000&pause=1000&color=58A6FF&center=true&vCenter=true&width=700&lines=Estudante+de+Ci%C3%AAncia+da+Computa%C3%A7%C3%A3o;JavaScript+%7C+TypeScript+%7C+Node.js;Aprendendo%2C+construindo+e+evoluindo"
    alt="Animação de texto"
  />

  <br />

  <a href="https://github.com/edsom-junior">
    <img src="https://img.shields.io/badge/GitHub-edsom--junior-0D1117?style=for-the-badge&logo=github&logoColor=58A6FF" alt="GitHub" />
  </a>
  <a href="https://www.linkedin.com/in/edsom-junior-rodrigues-cassamali-08a291309/">
    <img src="https://img.shields.io/badge/LinkedIn-Conectar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="https://www.instagram.com/juni0r_rc/">
    <img src="https://img.shields.io/badge/Instagram-Perfil-161B22?style=for-the-badge&logo=instagram&logoColor=58A6FF" alt="Instagram" />
  </a>

</div>

---

## `> Sobre mim`

Olá! Sou **Edsom Junior**, estudante de Ciência da Computação.

Tenho interesse em desenvolvimento de software, principalmente no ecossistema JavaScript, TypeScript e Node.js, além de trabalhar com SQL.

Meu GitHub reúne projetos de diferentes etapas da minha formação: desde exercícios acadêmicos em C# e Python até projetos de desenvolvimento de software. Também utilizo esse espaço para praticar conceitos, explorar soluções e acompanhar minha evolução como programador.

Gosto de entender como as coisas funcionam por trás do código e transformar o conhecimento adquirido em projetos práticos.

```js
const edsom = {
  nome: "Edsom Junior",
  area: "Ciência da Computação",
  foco: ["JavaScript", "TypeScript", "Node.js"],
  bancoDeDados: ["SQL"],
  estudos: ["C#", "Python"],
  github: "edsom-junior",
  objetivo: "Aprender, construir e evoluir através de projetos"
};


### Importante: ativar a animação Snake

O restante do README usa imagens externas para gerar as estatísticas e animações. A Snake, porém, precisa de uma GitHub Action para criar os arquivos SVG na branch `output`. Adicione também o arquivo `.github/workflows/snake.yml` ao repositório do perfil, com este conteúdo:

```yaml
name: Generate contribution snake

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:
  push:
    branches:
      - main

permissions:
  contents: write

jobs:
  generate:
    runs-on: ubuntu-latest

    steps:
      - name: Generate snake
        uses: Platane/snk@v3
        with:
          github_user_name: edsom-junior
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: Publish snake
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
