# Site — Roberto Franco Moreira

Site estático (Hugo) com cursos, projetos e materiais didáticos. Tema próprio, sem dependências externas.

## Estrutura

- `content/cursos/` — uma página `.md` por disciplina (ementa, programa, seção Materiais)
- `content/projetos/` — projetos de pesquisa e livros
- `content/sobre.md` — bio
- `layouts/` + `assets/css/main.css` — tema (não precisa mexer para editar conteúdo)
- `hugo.toml` — configuração; trocar `baseURL` pelo domínio definitivo antes de publicar

## Ver localmente

```
hugo server
```

Abre em http://localhost:1313 e recarrega a cada edição.

## Adicionar materiais a um curso

Na seção `## Materiais` da página do curso, listar links. PDFs pesados ficam no
Google Drive (link de compartilhamento); textos leves podem ir em `static/`
(ex.: `static/pdf/aula1.pdf` vira `/pdf/aula1.pdf`).

## Publicar (GitHub Pages, gratuito)

1. Criar repositório no GitHub (ex.: `site`) e subir esta pasta.
2. No repositório: Settings → Pages → Build and deployment → GitHub Actions.
3. Usar o workflow oficial "Hugo" sugerido pelo GitHub (ele roda `hugo` e publica `public/`).
4. Ajustar `baseURL` no `hugo.toml` para a URL final.
5. Domínio próprio (opcional, ~R$ 40/ano no registro.br): Settings → Pages → Custom domain, e apontar o DNS (CNAME) para `<usuario>.github.io`.

O Moodle/e-Disciplinas não hospeda nada disso: as páginas dos cursos aqui são o
lar dos materiais, e no Moodle entra só o link.
