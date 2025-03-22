Olá, eu sou Elizângela Bezerra da Silva! 👋
🌟 Bem-vindo(a) ao meu GitHub!

## 🚀 Sobre Mim:
🎓 Formada em Análise de Sistemas
💻 Apaixonada por tecnologia, resolução de problemas e aprendizado contínuo.

## 
- 🔭 Atualmente estou trabalhando em projetos utilizando Node.js, React.js, TypeScript, Docker, SQL e NoSQL.
- 🌱 Estou aprendendo novas tecnologias e aprimorando minhas habilidades em desenvolvimento web.
- 👯 Procurando colaborar em projetos open-source e iniciativas comunitárias.
- 🤔 Estou procurando ajuda com melhorias de desempenho em aplicações web.
- ⚡ Curiosidade: Além de programar, adoro cozinhar e praticar esportes ao ar livre.





 
<div> 
  <a href="https://instagram.com/rafaballerini" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
 <a href="https://discord.gg/wagxzStdcR" target="_blank"><img src="https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white" target="_blank"></a> 
  <a href = "mailto:contatorafaballerini@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
  <a href="https://www.linkedin.com/in/rafaella-ballerini-45875016a" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>   
</div>

name: Generate Snake Animation

on:
  schedule:
    # Executa a cada 6 horas
    - cron: "0 */6 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout the repository
        uses: actions/checkout@v2

      - name: Generate Snake Animation
        uses: Platane/snk@master
        with:
          github_user_name: E-l-y
          outputs: dist/snake.svg

      - name: Push Snake Animation to the repository
        uses: EndBug/add-and-commit@v7
        with:
          author_name: github-actions
          author_email: github-actions@github.com
          message: "Update Snake Animation"
          add: dist/snake.svg

      - name: Deploy Snake Animation
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./dist





  
