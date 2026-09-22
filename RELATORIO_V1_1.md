# MinhaFrequência v1.1 — revisão UX orientada por perfis de estudantes

## O que mudou
A v1.1 implementa a revisão solicitada a partir de cinco perfis simulados de estudantes: noturno que trabalha, diurna altamente organizada, estudante que busca previsibilidade, estudante com maior necessidade de legibilidade e veterano pragmático.

## 1. Andamento da disciplina
Foi introduzido um modelo distinto da frequência:
- encontros previstos no controle;
- encontros transcorridos;
- encontros realizados estimados;
- encontros restantes;
- cancelamentos registrados como "não houve aula";
- reposições cadastradas;
- quantidade de registros de frequência.

O cálculo de andamento não transforma falta em aula não ocorrida. Uma data regular passada conta como encontro realizado estimado, exceto quando existe registro de "não houve aula". Reposições passadas somam ao andamento, limitado ao total previsto.

## 2. Home
O antigo banner de risco foi substituído por um aviso compacto, sem triângulo, exibido somente quando uma UC tem frequência abaixo de 85% ou margem estimada de até 1 encontro.
O aviso fica junto ao bloco de frequência, nunca acima de "Próxima aula".

## 3. Cards das disciplinas
Cada disciplina passou a mostrar:
- monograma;
- dia, horário e sala;
- encontros realizados / previstos;
- quantos encontros restam;
- barra de andamento;
- frequência em percentual;
- próximo compromisso, quando houver.

## 4. Frequência
A tela separa:
- Andamento estimado da disciplina;
- Frequência do estudante.

Cada card mostra:
- progresso realizado/previsto;
- encontros restantes;
- cancelamentos e reposições, quando existentes;
- horas de ausência;
- margem estimada;
- número de registros;
- projeção de frequência caso haja nova falta de 4h.

A projeção não altera registros reais.

## 5. Programa da disciplina
O modal foi reconstruído:
- textarea com contraste revisado;
- labels mais fortes;
- campo de arquivo próprio em vez do controle nativo cru;
- suporte local a TXT, MD e CSV;
- nome do arquivo carregado e opção de remover;
- bloco de privacidade;
- pré-visualização;
- contadores de encontros previstos, tópicos identificados, associados e sem assunto;
- confirmação obrigatória para distribuição sequencial quando não há datas;
- confirmação antes de substituir assuntos já salvos.

O texto original do programa passa a ser salvo localmente em programSources.

## 6. Contraste do modo escuro
Nova hierarquia:
- fundo: #2B5870
- superfície: #356B82
- superfície secundária: #427D92
- superfície elevada: #4E8CA0
- campo: #3C748A
- texto principal: #FFF7E8
- texto secundário: #E0E8E8
- borda forte: #8AB0BD

O modo escuro permanece azul-petróleo e não usa preto como base.

## 7. Dados e migração
schemaVersion: 2.
Mantida a chave localStorage existente: minhafrequencia_v03.
A migração preserva dados anteriores e acrescenta programSources.

## Validação técnica
- JavaScript compilado sem erro de sintaxe.
- Não há junções duplicadas de declarações de função.
- Service worker versionado para minhafrequencia-v1.1.0.
- GitHub Pages recompila automaticamente após os commits.
