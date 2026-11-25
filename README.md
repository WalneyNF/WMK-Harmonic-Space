# 🚀 WMK Harmonic Space — Simulador Espacial 3D

![Logotipo WMK Harmonic Space](assets/logo.svg)

**Versão 0.5.0 — 25/11/2026** · Protótipo independente desenvolvido com **HTML, CSS, JavaScript e WebGL**, sem Docker, compilação, bibliotecas CDN ou dependência de IA.

**Autor:** Walney Moreira Klein — [walneyk@hotmail.com](mailto:walneyk@hotmail.com)

## Ideia do jogo

Um simulador de espaçonaves centrado em **pilotagem, hangar, evolução tecnológica, exploração e futura construção de naves**. O sistema musical é **somente uma recarga auxiliar de emergência** quando a energia ficar crítica; não faz parte da interface normal de voo.

## Como começar

1. Baixe o projeto como ZIP no GitHub e extraia numa pasta.
2. Abra `index.html` no Google Chrome/Edge com WebGL ativo.
3. Escolha uma das **três facções espaciais originais** no hangar.
4. Inspecione uma nave disponível, selecione **Testar voo** e experimente os controles.
5. Utilize o botão **Árvore tecnológica** para pesquisar modelos de nível II e III.

Não é necessário iniciar um servidor. Os JSONs são editáveis na pasta `naves/` e podem ser importados individualmente pelo hangar; o arquivo `naves.js` mantém um catálogo incorporado para uso offline.

## Controles

| Controle | Função |
|---|---|
| W / S | Acelerar / desacelerar |
| A / D | Deslocar lateralmente e inclinar até 30° para o mesmo lado |
| Q / E | Girar o bico à esquerda / direita (guinada) |
| C / X | Subir / descer |
| Espaço | Frear |
| J, K, L, Ç / ; | Pulsos musicais **exclusivamente na recarga de emergência** |

A inclinação é suavizada por interpolação exponencial (*lerp* independente de FPS) e retorna lentamente à horizontal ao soltar a tecla. A câmera externa permanece atrás e acima da nave; distância e altura são configuráveis por modelo.

## Nações fictícias e árvore tecnológica

| Facção | Identidade | Nível I | Nível II | Nível III |
|---|---|---|---|---|
| Confederação Hélion | Exploração e ciência | Orion | Lyra | Aurora Prime |
| Domínio Véspera | Velocidade e defesa | Vega | Nyx | Spectra |
| União Arkheon | Mineração e indústria | Atlas | Ferrox | Colossus |

As naves de nível I são liberadas desde o início. Cada linha requer a nave anterior e créditos de pesquisa. O hangar possui um botão de **créditos de teste** para validar níveis superiores sem esperar missões futuras. Os modelos de nível II e III ainda utilizam geometrias procedurais derivadas dos três chassis básicos — são visualmente diferenciados, **não modelos GLB finalizados**.

## Arquivos importantes

- `index.html` — interface de pilotagem, hangar e árvore tecnológica.
- `game.js` — movimento, energia, missão, controles e recarga de emergência.
- `space3d.js` — renderizador WebGL, cenários, hangar e geometrias procedurais.
- `hangar.js` — nações, catálogo, pesquisa e salvamento da frota.
- `naves/*.json` — parâmetros físicos e características individuais de **9 espaçonaves**.
- `nacoes/*.json` — definições das **3 facções fictícias**.
- `naves.js` — catálogo compilado para execução offline.
- `assets/logo.svg` e `assets/logo.png` — marca original do projeto.
- `pesquisa.html` — análise dos jogos espaciais de referência (não estão incluídos nem copiados).
- `roadmap.html` — prioridades e estágios do projeto.
- `manuais/primeiro-contato.html` — primeiro voo e uso do hangar.

## Limitações da versão

O renderizador é um WebGL básico próprio; ainda não há modelos 3D externos, texturas PBR, física orbital, colisão realista, interiores navegáveis, batalhas, mineração, mercado ou multiplayer. A árvore e os créditos são um **protótipo funcional de progressão**, com recompensa inicial de atracagem e créditos de teste. A versão foi criada para validar ergonomia, direção visual e arquitetura de conteúdo antes de investir em ativos detalhados.

## Licença

Código original e identidade visual deste projeto sob a [licença MIT](LICENSE). Nomes e propriedades dos jogos de referência pertencem aos respectivos titulares.
