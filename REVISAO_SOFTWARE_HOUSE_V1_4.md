# MinhaFrequência v1.4 — reflexão da software house

## Arquitetura
A v1.4 não altera o schema de dados. Os novos filtros são estado efêmero de interface e não devem ser persistidos no localStorage. Isso evita migrações desnecessárias e reduz risco sobre dados já cadastrados.

## Estratégia técnica
1. Uma única função gera os itens do histórico.
2. Uma função de predicado aplica todos os filtros.
3. A busca textual é normalizada para caixa e acentos.
4. Filtros combinam-se em lógica E.
5. Motivo só é exibido quando a situação selecionada o comporta.
6. "Compromisso" consulta eventos associados à mesma disciplina/data e também reposições/aulas externas.
7. O histórico continua sendo a fonte de edição; os filtros nunca criam ou modificam registros.

## UX mobile
- Essenciais: busca por assunto, disciplina, situação.
- Avançados: período, intervalo, compromisso, motivo, próximas aulas.
- "Mais filtros" usa progressive disclosure para não sobrecarregar iPhone pequeno.
- Chips ativos dão visibilidade ao estado do filtro.
- "Limpar" restaura uma consulta previsível.

## Critérios de aceitação
- "Economia + Falta" funciona.
- "Todas + Sem registro + agosto" funciona.
- busca "elasticidade" encontra assunto independentemente de maiúsculas/acento;
- "Não houve aula + Professor(a) cancelou" funciona;
- "Prova + setembro" encontra aulas ligadas a prova;
- intervalo personalizado respeita data inicial/final;
- ✓4h, ◐2h e edição continuam operando na lista filtrada;
- nenhum filtro transforma ausência de registro em falta;
- JavaScript passa validação sintática antes do deploy.
