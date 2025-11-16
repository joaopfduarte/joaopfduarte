# Olá! 👋 Eu sou o joaopfduarte

Sou desenvolvedor(a) interessado(a) em backend, APIs e automação. Aqui mostro meus projetos, estatísticas e atividade no GitHub.

<!--PROFILE BADGES-->
![Follow](https://img.shields.io/github/followers/joaopfduarte?label=Seguir&style=social)
![Repos](https://img.shields.io/github/repo-size/joaopfduarte/joaopfduarte?color=blue)
![Twitter Follow](https://img.shields.io/twitter/follow/joaopfduarte?style=social)

<!--START_SECTION:activity-->
Última atualização: <!--LAST_UPDATE-->
<!--END_SECTION:activity-->

## 🚀 Sobre
- Linguagens preferidas: Python, JavaScript, Go
- Gosto de: APIs, automação e arquitetura escalável
- Contato: [LinkedIn](https://linkedin.com/in/joaopfduarte) • [Site pessoal](https://seusite.example)

## 📊 Minhas estatísticas
![Estatísticas do GitHub](https://github-readme-stats.vercel.app/api?username=joaopfduarte&show_icons=true&theme=radical)

![Top Linguagens](https://github-readme-stats.vercel.app/api/top-langs/?username=joaopfduarte&layout=compact&theme=radical)

![Troféus](https://github-profile-trophy.vercel.app/?username=joaopfduarte&theme=radical)

![Streak](https://github-readme-streak-stats.herokuapp.com/?user=joaopfduarte&theme=dark)

## 📌 Repositórios em destaque
> Use a interface de perfil do GitHub para "pin" os repositórios abaixo.
- nome-do-repo-1 — descrição curta
- nome-do-repo-2 — descrição curta
- nome-do-repo-3 — descrição curta

## 🧰 Ferramentas e recursos úteis
- Geradores de README: readme.so, awesome-github-profile-readme
- Cards: github-readme-stats, github-profile-trophy, github-readme-streak-stats
- Badges: shields.io
- Para commits automáticos de "heartbeat": GitHub Actions (usar GITHUB_TOKEN)

---

Se quiser eu adapto esse README com seu texto real, seus repos favoritos ou adiciono outras integrações (WakaTime, LeetCode, etc.).````

E aqui está um exemplo simples de workflow (coloque em .github/workflows/update-readme.yml) que atualiza a tag <!--LAST_UPDATE--> no README diariamente e faz commit — isso ajuda a manter o gráfico de contribuições “ativo” sem expor segredos:

```name=.github/workflows/update-readme.yml
name: Atualizar README (timestamp diário)

on:
  schedule:
    - cron: '0 0 * * *' # diário UTC à meia-noite
  workflow_dispatch:

jobs:
  update-readme:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
        with:
          persist-credentials: true

      - name: Atualizar timestamp no README
        run: |
          TIMESTAMP="$(date -u +"%Y-%m-%d %H:%M:%S UTC")"
          # substitui o placeholder <!--LAST_UPDATE--> por texto com timestamp
          perl -0777 -pe "s/<!--START_SECTION:activity-->.*?<!--END_SECTION:activity-->/<!--START_SECTION:activity-->\\nÚltima atualização: $TIMESTAMP\\n<!--END_SECTION:activity-->/s" -i README.md

      - name: Commit e push
        run: |
          git config user.name "github-actions[bot]"
          git config user.email "41898282+github-actions[bot]@users.noreply.github.com"
          git add README.md
          git commit -m "chore: atualizar timestamp do README" || echo "Sem mudanças para commitar"
          git push
```

Dicas rápidas finais
- Pinned repos: escolha projetos com README atraente e demos.
- Menos é mais: não sobrecarregue com imagens/gifs que poluem a leitura.
- Teste os cards: alguns serviços podem cair ocasionalmente; mantenha alternativas.
- Segurança: não coloque tokens públicos. Use actions que usam GITHUB_TOKEN (já seguro).
- Inspiração: visite perfis como os de pessoas que você curte e examine o README (clique em “Edit” para ver a fonte).

Quer que eu:
- personalize o README acima com sua bio real e repos destacados?
- gere o conteúdo pronto para você copiar/colar (ou eu criar os arquivos no repo, se você me der permissão)?

Diga qual das opções prefere e eu adapto/prossigo.
