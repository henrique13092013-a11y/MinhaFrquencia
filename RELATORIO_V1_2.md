# MinhaFrequência v1.2 — implementação após revisão mobile

## Processo
Antes da implementação, foi registrada a revisão simulada de especialista mobile em REVISAO_ESPECIALISTA_MOBILE_V1_2.md. A v1.2 aplica as decisões prioritárias dessa revisão.

## Principais mudanças

### 1. Página própria da disciplina
Cada UC agora pode ser aberta como uma página de profundidade, com:
- identidade por cor e monograma;
- professor(a), horário e sala;
- andamento realizado/previsto;
- frequência e horas ausentes;
- margem estimada;
- próximos compromissos;
- linha do tempo dos encontros;
- assuntos já associados;
- indicação de aulas sem registro;
- atalhos para Programa e Mapa de salas.

### 2. Pendências de registro
Aulas regulares já transcorridas sem registro são mostradas como “Pendências”.
Elas não são convertidas em falta.
A aula do dia só entra como pendência depois do horário final previsto.

### 3. Registro rápido
“Fui 4h” e “Fui 2h” passam a ser ações de um toque na Home.
“Faltei” continua abrindo o fluxo com motivo.
O registro rápido oferece “Desfazer”.

### 4. Undo
Presença, edição de registro e conclusão de atividade oferecem ação temporária “Desfazer”.

### 5. Home simplificada
Os cards de disciplina viram resumos navegáveis:
- nome;
- dia/horário/sala;
- realizado/previsto;
- encontros restantes;
- frequência;
- barra de andamento.
Detalhes migram para a página da UC.

### 6. Atividades por necessidade de ação
A lista prioriza:
- atrasadas;
- hoje;
- amanhã;
- prova/exame/entrega dentro da mesma janela.
Isso muda ordenação sem transformar todo item urgente em alerta visual.

### 7. Tipografia
Metadados funcionais receberam reforço de tamanho onde necessário.
A v1.2 mantém 10 px apenas para conteúdo terciário.

### 8. Persistência
schemaVersion: 3.
A chave localStorage continua sendo minhafrequencia_v03.
Não há reinicialização de perfil, disciplinas, salas, frequência, eventos, programa ou tema.

### 9. PWA
Service worker: minhafrequencia-v1.2.0.
