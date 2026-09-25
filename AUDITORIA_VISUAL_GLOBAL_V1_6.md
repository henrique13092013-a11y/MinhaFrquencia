# MinhaFrequência v1.6 — Auditoria visual global

## Escopo
A revisão foi aplicada à ferramenta inteira, não apenas à legenda do calendário. O objetivo foi remover dependência de métricas tipográficas para ícones estruturais e estabelecer regras únicas de alinhamento.

## Cobertura estática
- 128 instâncias de botão identificadas no HTML/JS.
- 21 botões sem classe própria revisados por contexto e cobertos por seletor do componente pai.
- 43 botões com SVG estático/dinâmico cobertos pelo sistema de slots vetoriais.
- 2 botões com emoji de conteúdo preservados (Programa e Sala), ambos dentro de slot fixo.
- 9 chips da legenda do calendário reconstruídos com uma única estrutura visual.

## Componentes auditados
- topo e identificação do semestre;
- navegação de calendário e date picker;
- seletor Semana/Mês;
- legenda do calendário;
- marcações de presença, parcial, falta, sem aula, EaD, outro horário e aula externa;
- marcações de eventos no calendário;
- navegação inferior;
- atalhos da Home;
- cards de hoje e próxima aula;
- pendências;
- histórico de frequências;
- filtros e chips;
- cards de frequência e simulação;
- página de disciplina;
- timeline;
- mapa de salas;
- configurações;
- onboarding;
- seletores de termo/semestre/ano;
- overlays/modais;
- opções de presença e motivos;
- botões primários, secundários, editar, excluir, salvar e fechar;
- catálogo de disciplinas;
- importação de programa;
- toast e ações de desfazer.

## Regras introduzidas
1. Ícones estruturais usam SVG, não caracteres de fonte.
2. Cada contexto tem slot dimensional fixo.
3. Ícone e texto compartilham uma linha óptica controlada.
4. Botões de ação são centralizados; cards/linhas editoriais permanecem alinhados à esquerda.
5. Emojis são mantidos apenas como conteúdo e recebem caixa fixa.
6. Setas, fechar, check, parcial, falta, EaD, menu e navegação usam geometria consistente.
7. O calendário usa os mesmos desenhos no chip de legenda e no marcador da data.

## Compatibilidade
- schemaVersion permanece 3.
- localStorage permanece minhafrequencia_v03.
- nenhum dado acadêmico foi migrado ou regravado.

## Validação
- JavaScript completo validado por new Function sem erro.
- tags style balanceadas.
- nenhuma seta tipográfica ‹ › restante.
- nenhum símbolo ◐ restante como ícone de interface.
- nenhum × tipográfico restante como botão de fechar.
- os emojis de Prova/Seminário/Entrega/Institucional foram removidos da legenda estrutural e substituídos por SVG; emojis continuam nos conteúdos.
- cache PWA atualizado para minhafrequencia-v1.6.0.