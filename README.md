# 🚀 WMK Harmonic Space — Simulador Espacial 3D

![Logotipo WMK Harmonic Space](assets/logo.svg)

**Versão 0.5.0 — 25/11/2026** · Protótipo em **HTML, CSS, JavaScript e WebGL**, sem Docker ou dependência de IA.

**Autor:** Walney Moreira Klein — [walneyk@hotmail.com](mailto:walneyk@hotmail.com)

## Conceito

**Jogo de espaçonaves 3D** focado em pilotagem, hangar, exploração e progressão tecnológica. A música **não faz parte da jogabilidade normal**: é apenas um mecanismo de **recarga emergencial da bateria**, disponível quando a energia fica crítica.

## Como testar

1. Clique em **Code → Download ZIP**, extraia o projeto e abra `index.html` no Chrome ou Edge com WebGL.
2. Escolha uma das três nações fictícias e uma nave no hangar.
3. Clique em **Testar voo** e pilote com os comandos abaixo.
4. Abra a **Árvore tecnológica** para experimentar os níveis e desbloqueios.

## Controles

| Tecla | Função |
|---|---|
| W / S | Acelerar / reduzir velocidade |
| A / D | Deslocamento lateral com inclinação visual de até 30° para o mesmo lado; retorno suave ao soltar |
| Q / E | Guinada: girar o bico à esquerda / direita |
| C / X | Subir / descer |
| Espaço | Frear |
| J, K, L, Ç / ; | Somente quando a recarga de emergência estiver aberta |

## Nações, tipos de naves e níveis

| Nação fictícia | Especialização | Nível I | Nível II | Nível III |
|---|---|---|---|---|
| Confederação Hélion | Exploração e ciência | Orion — exploradora | Lyra — pesquisa | Aurora Prime — colonizadora |
| Domínio Véspera | Mobilidade e defesa | Vega — interceptora | Nyx — caça tático | Spectra — fragata |
| União Arkheon | Indústria e mineração | Atlas — cargueira | Ferrox — mineradora | Colossus — industrial |

As nove naves possuem JSON individual em `naves/`. As facções possuem definição em `nacoes/`. A árvore tecnológica exige nave anterior e créditos de pesquisa. O botão de créditos de teste existe apenas para facilitar a avaliação da versão.

## Organização

- `index.html`: interface e cena principal
- `game.js`: controles, voo, energia, missão e recarga
- `space3d.js`: renderizador WebGL e geometria 3D
- `hangar.js`: garagem, nações e árvore tecnológica
- `naves.js`: catálogo embutido para funcionamento offline
- `naves/*.json`, `nacoes/*.json`: dados individuais
- `assets/logo.svg` e `assets/logo.png`: identidade visual
- [`pesquisa.html`](pesquisa.html): jogos espaciais de referência
- [`roadmap.html`](roadmap.html): plano de desenvolvimento
- [Manual primeiro contato](manuais/primeiro-contato.html)
- [Histórico de alterações](CHANGELOG.md)

## Situação e limitações

A v0.5.0 apresenta modelos procedurais, hangar industrial, seleção de facção, árvore tecnológica inicial, A/D corrigidos, Q/E independentes e recarga emergencial contextual. **Ainda não existem interiores, modelos GLB acabados, física orbital completa, mineração, combate, multiplayer ou construção modular**. Esses recursos estão planejados no roadmap.

## Licença e créditos

Código e materiais visuais originais sob [MIT](LICENSE).

**Walney Moreira Klein — walneyk@hotmail.com**
