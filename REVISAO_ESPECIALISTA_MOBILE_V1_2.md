# Revisão simulada — especialista sênior em apps mobile / iOS

Escopo: MinhaFrequência v1.1 como PWA iPhone-first.

## Diagnóstico principal

A v1.1 já tem boa base funcional, mas a próxima evolução não deve adicionar mais informação à Home. O maior problema arquitetural é a ausência de uma tela de detalhe da disciplina: frequência, progresso, cronograma, assuntos, eventos e sala estão distribuídos por telas diferentes. Em mobile, isso aumenta carga cognitiva e faz os cards da Home crescerem indefinidamente.

## Decisões recomendadas antes da v1.2

1. **Criar uma tela de disciplina em profundidade**
   - página própria, não modal;
   - identidade da UC, horário, professor(a), sala;
   - andamento e frequência como métricas distintas;
   - linha do tempo de encontros;
   - assuntos do programa e próximos compromissos;
   - atalhos para programa, edição e registro.

2. **Transformar aulas passadas sem registro em pendências**
   - nunca inferir falta;
   - não exibir quando não houver pendências;
   - card compacto na Home;
   - toque leva diretamente ao registro daquela aula.

3. **Reduzir densidade dos cards da Home**
   - card de disciplina deve servir de resumo + navegação;
   - detalhes migram para a página da UC;
   - manter andamento e frequência como leitura de relance.

4. **Feedback imediato e reversível**
   - presença integral/parcial deve poder ser registrada em um toque;
   - feedback com ação “Desfazer” por alguns segundos;
   - faltas continuam exigindo motivo;
   - conclusão de atividade também deve oferecer “Desfazer”.

5. **Priorizar atividades por necessidade de ação**
   - atrasadas primeiro;
   - hoje/amanhã em seguida;
   - prova/exame/entrega ganham prioridade dentro da mesma janela;
   - não transformar tudo em alerta vermelho.

6. **Tipografia**
   - evitar metadados funcionais abaixo de 11 px;
   - 12 px para informação que precisa ser lida;
   - manter 10 px apenas para elementos realmente terciários.

7. **Navegação**
   - Home continua sendo panorama;
   - Agenda continua sendo temporal;
   - Frequência continua sendo analítica;
   - Disciplina vira o ponto de profundidade;
   - Ajustes continuam administrativos.

8. **PWA**
   - manter a stack atual;
   - preservar dados;
   - versionar cache;
   - não mudar schema sem migração.

## Critério de aceitação da v1.2

A Home deve ficar mais simples mesmo com mais funcionalidade. O aluno deve conseguir:
- registrar presença integral/parcial em 1 toque;
- identificar aulas sem registro sem confundi-las com faltas;
- abrir qualquer disciplina e ver, em uma única tela, andamento, frequência, cronograma e próximos compromissos;
- desfazer ações recentes;
- ler a interface confortavelmente em iPhone pequeno.

Esta revisão é uma simulação técnica de especialista, não uma avaliação de um profissional externo contratado.
