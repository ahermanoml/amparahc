# Handoff: Site Ampara Home Care

## Overview
Site institucional one-page da **Ampara Home Care** (Tupaciguara/MG e região), focado em captar clientes/famílias via WhatsApp. Serviços: cuidadores em casa (escalas de 6/8/12/24h), acompanhamento pontual (consultas, internações, exames) e procedimentos de enfermagem avulsos. Coordenação: 1 médico (Dr. Antônio Hermano) + 2 enfermeiros (Viviane e Cristiano).

## About the Design Files
Os arquivos deste pacote são **referências de design criadas em HTML** — não código de produção. A tarefa é **recriar este design no ambiente do repositório de destino** usando seus padrões existentes; se não houver ambiente definido, um site estático simples (HTML/CSS puro ou Astro/Next static) é suficiente — é uma landing page sem backend.

O arquivo `site-standalone.html` é autocontido (imagens/fontes embutidas) e abre direto no navegador — **é a referência visual canônica**. `Ampara Home Care.dc.html` é o fonte original (usa um runtime proprietário; leia o markup/estilos, não execute).

## Fidelity
**High-fidelity**: cores, tipografia, espaçamentos e copy são finais. Recriar fielmente.

## Design Tokens
- Azul marca: `#0a7ba7` (hero bg, títulos, header logo)
- Azul escuro (gradiente contato): `#075e80`
- Rosa/pink CTA: `#d61f7f` (hover `#ef2f92` em fundo escuro, `#b71469` no header)
- Texto principal: `#17333e` · secundário: `#44606c` · claro sobre azul: `#cfe8f2` / `#a8d6e6`
- Fundos: página `#f6f8f9`, cards `#ffffff`, chips `#f0f6f8`, tint azul `#e2f2f8`, tint rosa `#fbe3ef`, footer `#eef3f5`
- Bordas: `#e3ebee`, chips `#dbe8ec`
- Fontes: **Bricolage Grotesque** (títulos, 600–700) + **Nunito Sans** (corpo) — Google Fonts
- Radius: cards 18px, pills/botões 999px, blocos grandes 28px, hero foto 24px
- Sombra cards: `0 4px 16px rgba(10,123,167,0.06)`
- Container: max-width 1120px, padding lateral 24px
- Scroll suave (`scroll-behavior: smooth`), âncoras: #inicio #servicos #como-funciona #equipe #faq #contato

## Screens / Sections (ordem)
1. **Header sticky** — fundo `rgba(246,248,249,0.92)` + blur; logo texto "AMPARA" (Bricolage 700, 22px, letter-spacing .12em, azul) + "HOME CARE" (12px, .28em, rosa); nav (Serviços, Como funciona, Equipe, Dúvidas); botão pill rosa "Falar no WhatsApp".
2. **Hero** (#inicio) — fundo azul `#0a7ba7`, grid 1.1fr/0.9fr, gap 56px, padding 72/24/80. Esquerda: logo (imagem, 340px), h1 46px "Cuidado profissional, no lugar onde seu familiar se sente melhor: em casa.", parágrafo 19px `#cfe8f2` ("Cuidadores certificados na escala que a sua família precisa — de 6 a 24 horas — com avaliação inicial feita pessoalmente por médico ou enfermeiro. Atendemos Tupaciguara e região."), CTA pill rosa "Conversar agora no WhatsApp". Direita: foto (420px alto, radius 24, sombra grande) com badge branco flutuante embaixo-esquerda: "Primeira visita: médico ou enfermeiro" / "Avaliação completa antes de começar". Animação fadeUp 0.7s no load.
3. **Serviços** (#servicos) — eyebrow rosa "SERVIÇOS" (13px, .24em), h2 34px azul "Dois jeitos de cuidar: contínuo em casa ou pontual, quando precisar". Grid 2 colunas, gap 22px:
   - Card 1 (badge tint azul "CUIDADO CONTÍNUO EM CASA"): título "Cuidador em casa, na escala que a família precisar"; checklist ✓ azul: escalas 6/8/12/24h por dia · todos os dias ou só dias de semana · avaliação inicial presencial médico ou enfermeiro · acompanhamento contínuo da evolução.
   - Card 2 (badge tint rosa "ACOMPANHAMENTO PONTUAL"): título "Cuidador para consultas, exames e internações"; checklist ✓ rosa: acompanhamento em consultas médicas · acompanhamento durante internação na Policlínica · exames (coleta de sangue) com transporte e retorno.
   - Card full-width (badge azul "PROCEDIMENTOS DE ENFERMAGEM AVULSOS"): título "Precisa só de um procedimento? A gente vai até você"; chips pill: Banho no leito, Banho com auxílio, Troca de sonda vesical, Troca de sonda nasoenteral / GTT, Curativos, Medicação intramuscular, Medicação endovenosa / soro, Aspiração traqueal. "Valores sob consulta pelo WhatsApp."
   - Faixa tint azul (`#e2f2f8`, borda `#c3e2ee`): avatar círculo azul "A" + texto: "**Em todos os serviços**, um médico ou enfermeiro da coordenação está a par do caso e gerencia o atendimento — mesmo sem contato direto com o paciente, dá suporte ao cuidador sempre que for preciso."
4. **Como funciona** (#como-funciona) — bloco azul radius 28, 3 colunas, números 44px `#7fc9e0`: 1) "Você chama no WhatsApp" (conte o que precisa: cuidado no dia a dia, acompanhamento em consulta ou internação, ou procedimento avulso); 2) "Avaliação ou agendamento" (contínuo começa com visita de médico ou enfermeiro; pontuais agendados direto); 3) "Atendimento com supervisão" (profissional certificado pela Ampara, sempre com médico ou enfermeiro a par do caso).
5. **Equipe** (#equipe) — eyebrow "QUEM COORDENA", h2 "Três profissionais de saúde à frente de cada cuidado", sub: "A Ampara não é uma agência de indicação...". 3 cards centrados com foto circular 120px: Dr. Antônio Hermano (MÉDICO · COORDENADOR, azul), Viviane (ENFERMEIRA · COORDENADORA, rosa), Cristiano (ENFERMEIRO · COORDENADOR, azul). Bios no HTML.
6. **FAQ** (#faq, max-width 780px) — `<details>` cards: como funciona a primeira visita · cuidadores são de confiança · quais cidades · valores (contínuo = proposta pós-avaliação; pontuais = valor na hora no WhatsApp) · não é só para idosos.
7. **Contato** (#contato) — bloco gradiente azul radius 28, centrado: h2 36px "Vamos conversar sobre o cuidado do seu familiar?", CTA pill rosa "Chamar no WhatsApp".
8. **Footer** — fundo `#eef3f5`, logo texto + "Tupaciguara/MG e região · (63) 99275-7021".

## Interactions & Behavior
- Todos os CTAs abrem `https://wa.me/5563992757021?text=<msg urlencoded "Olá! Gostaria de saber mais sobre os serviços da Ampara Home Care.">` em nova aba. **Não exibir o número nos botões** (só no footer).
- Links âncora com scroll suave; hovers: links azul→rosa; botões rosa clareiam/escurecem (valores acima).
- FAQ: `<details>/<summary>` nativo, marcador "+" rosa à direita.
- Site é desktop-first (grids fixas de 2–3 colunas); **adicionar breakpoints mobile na implementação** (empilhar colunas <768px) — o protótipo não os define.

## Assets (pasta `assets/`)
- `logo-ampara.jpeg` — logo horizontal (fundo azul #0a7ba7; usada no hero sobre fundo azul)
- `hero-visita.jpeg` — foto hero (médico/enfermeira com paciente idosa, gerada por IA)
- `dr-antonio.jpeg`, `viviane.jpeg` — fotos da equipe (círculo 120px)
- Foto do Cristiano: conferir no standalone (foi arrastada no editor); se ausente, usar placeholder circular

## Files
- `site-standalone.html` — referência visual canônica (abrir no navegador)
- `Ampara Home Care.dc.html` — fonte original (ler markup/estilos)
- `assets/` — imagens
