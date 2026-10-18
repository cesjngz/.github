# Contexto — README de perfil da organização cesjngz

Essa pasta veio de uma sessão do Claude Code trabalhando no repositório
`cesjn-web` (site institucional da CESJN). O usuário pediu pra dar "a cara
do site" ao README do perfil da organização GitHub (`cesjngz`), e isso foi
continuado aqui porque o Claude daquela sessão não tinha acesso a esse
repositório `.github`.

## O que fazer com isto

1. Se o repositório `cesjngz/.github` ainda não existir, criar um
   repositório **público** chamado exatamente `.github` dentro da
   organização `cesjngz` (o nome exato é obrigatório — é assim que o
   GitHub identifica o repo de perfil da org). Precisa ser público pra que
   a imagem do logo (caminho relativo) e o README apareçam na página
   pública da organização.
2. Copiar o conteúdo desta pasta `profile/` (README.md + logo-azul.png)
   pra dentro de `profile/` na raiz desse repositório.
3. Commitar e dar push. A página `github.com/cesjngz` deve passar a
   mostrar esse README automaticamente (GitHub detecta `profile/README.md`
   nesse repo específico).

## Por que o caminho da imagem é relativo (`logo-azul.png`, não uma URL)

Na sessão anterior, tentamos usar
`https://raw.githubusercontent.com/cesjngz/cesjn-web/master/public/images/logo-azul.png`
pra puxar o logo direto do repo `cesjn-web`, mas essa URL retornou 404
publicamente — o repositório `cesjn-web` parece ser **privado**, e uma
imagem hospedada lá não aparece pra quem visita a página pública da
organização sem estar autenticado. Por isso o logo foi copiado pra dentro
desta pasta, pra o README referenciar um arquivo local (que resolve
automaticamente, já que o repo `.github` precisa ser público).

## Decisões de design já tomadas (não precisa redecidir)

- Cor de destaque usada nos badges (`244368`) é o azul oficial do site
  (`--accent` em `cesjn-web/src/app/globals.css`).
- Os três badges de redes sociais (Instagram, Facebook, YouTube) usam os
  handles reais, já confirmados pelo cliente:
  - Instagram: `@CE.SJN`
  - Facebook: `CESJN`
  - YouTube: `@CESJN`
- O link "Site oficial" fica como "_em breve_" (sem URL) — o site ainda
  não está no ar. Quando for ao ar, trocar pelo link real e, se fizer
  sentido, remover o texto "em breve".
- GitHub README não aceita `style=""` customizado (é removido pela
  sanitização), então não dá pra usar as cores exatas do site em texto —
  por isso o visual usa o logo + badges coloridos como aproximação da
  identidade visual, em vez de CSS.

## O que falta verificar (não dava pra testar sem acesso ao repo)

- Confirmar visualmente que o README renderiza certo na página da
  organização depois do push (logo aparecendo, badges carregando, layout
  centralizado ok).
- Se quiser, considerar adicionar um link funcional pro site assim que ele
  estiver no ar.
