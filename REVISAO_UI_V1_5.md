# MinhaFrequência v1.5 — UI Consistency Pass

## Objetivo
Consolidar a interface antes de novas funcionalidades, corrigindo desalinhamentos, centralização óptica de botões, alturas inconsistentes, textos funcionais pequenos e o comportamento das cores de disciplinas no modo escuro.

## Alterações aplicadas

### 1. Gramática de botões
- Ações reais passam a usar alinhamento horizontal e vertical explícito.
- Botões de ação primária/secundária, ajustes, onboarding, frequência, histórico e navegação de detalhe recebem alturas padronizadas.
- Botões de ícone passam a usar place-items:center.
- SVGs dentro de botões são tratados como blocos para eliminar deslocamentos de baseline.

### 2. Exceções editoriais
Permanecem propositalmente alinhados à esquerda:
- cards clicáveis;
- atalhos editoriais;
- linhas de pendência;
- alertas de risco;
- cards de disciplina;
- linhas de sala;
- disclosure “Mais filtros”;
- opções com ícone + texto que funcionam como linhas de ação.

### 3. Alturas de controle
- pequeno: 44 px;
- médio: 48 px;
- grande: 52 px.
Os componentes existentes foram mapeados para esses níveis sem alterar a estrutura de dados.

### 4. Legibilidade
Metadados funcionais relevantes foram elevados para 11 px onde estavam excessivamente pequenos, incluindo status do histórico, resumos, informações de filtro, metadados de configurações e estatísticas auxiliares.

### 5. Modo escuro e disciplinas
As cores originais das disciplinas continuam armazenadas sem alteração. No modo escuro, sua apresentação é suavizada por mistura com superfícies/lavanda, reduzindo conflito cromático sem perder identidade.

### 6. Compatibilidade
- schemaVersion permanece 3.
- chave de dados permanece minhafrequencia_v03.
- nenhuma frequência, disciplina, evento ou programa é migrado ou regravado por esta atualização.
- funcionalidades de v1.4.3 permanecem presentes.

## Validações realizadas
- JavaScript completo: sintaxe válida.
- ausência de duplicação acidental de funções.
- tags style balanceadas.
- cache PWA atualizado para minhafrequencia-v1.5.0.
- manifesto atualizado para a base escura #121827.

## Limitação de teste
A validação estrutural e sintática foi concluída. O ambiente de execução não permitiu baixar a página pública para uma bateria automatizada de screenshots em Chromium; portanto, a revisão final de aparência deve considerar observação direta no iPhone após o deploy.