# MinhaFrequência v1.0 — Auditoria, design system e validação

## Auditoria aplicada
- A interface anterior concentrava demais a identidade em violeta/azul muito escuro.
- Metadados e labels estavam pequenos em alguns contextos.
- Emojis haviam sido removidos de forma excessiva, reduzindo personalidade.
- A Home colocava atalhos antes de informações acadêmicas prioritárias.
- A identidade das disciplinas precisava ser consistente em Home, Agenda, Frequência e Ajustes.
- A tela de frequência era funcional, porém pouco gráfica.
- Formulários precisavam de targets, labels e ritmo mobile mais consistentes.

## Princípios v1.0
1. PWA iPhone-first, sem migração de stack.
2. Dark mode azul-petróleo médio, não preto.
3. Light mode creme/off-white.
4. Paleta luminosa inspirada em relações cromáticas modernas: azul-piscina, cobalto, coral, amarelo quente, verde, lavanda e rosa.
5. Estrutura por ícones vetoriais; conteúdo e humor por emojis pequenos.
6. Disciplina = cor + monograma + acento geométrico.
7. Hierarquia editorial antes de excesso de cards.

## Arquitetura da Home
Próxima aula → Hoje → Próximas atividades → Minha frequência → Minhas disciplinas → Atalhos.

## Design system
### Dark
- fundo: #214E67
- superfície: #295B72
- superfície secundária: #326980
- texto: #FFF5DD

### Light
- fundo: #F3E8D3
- superfície: #FFF8EA
- texto: #12334A

### Acentos
- piscina: #45C4D8
- cobalto: #2878D6
- coral: #F06A55
- amarelo: #F2C14E
- verde: #58A86D
- lavanda: #A58AE8
- rosa: #E47DA4

## Ergonomia
- navegação inferior: 48 px
- botão central: 56 px
- campos: 48 px
- fonte de campos: 16 px
- botões principais: 44–50 px ou mais
- safe-area e reduced-motion preservados

## Emojis
- mantidos em eventos e conteúdo;
- 14 px em contexto normal;
- 9 px para indicadores secundários do calendário;
- não substituem labels nem estados funcionais.

## Dados
A chave localStorage `minhafrequencia_v03` foi preservada.
A v1.0 introduz `schemaVersion: 1` e migração automática, preservando perfil, curso, disciplinas, professores, salas, frequência, eventos, tema e assuntos.

## Testes executados
- JavaScript validado sintaticamente.
- Renderização verificada em 320, 390 e 430 px.
- Sem overflow horizontal nos tamanhos testados.
- Home verificada em claro e escuro.
- Agenda mensal verificada.
- Frequência verificada.
- Onboarding e Monte sua semana verificados.
- Inputs de Monte sua semana: 48–49 px, fonte 16 px.

## Painel simulado — decisões incorporadas
- estudantes: leitura rápida, sala e próxima aula mais evidentes;
- professor/secretaria: metadados explícitos e sem títulos acadêmicos desnecessários;
- Product Design iOS: hierarquia, targets, navegação e densidade ajustados;
- acessibilidade: foco visível, reduced motion e informação independente de cor;
- Design Systems: tokens e papéis cromáticos consolidados;
- engenharia: migração local, cache versionado e PWA mantida.
