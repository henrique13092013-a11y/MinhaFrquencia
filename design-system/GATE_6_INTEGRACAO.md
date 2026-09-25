# MinhaFrequência v1.7 — Gate 6

## Objetivo
Integrar no aplicativo real o design system aprovado nos Gates 3, 4 e 5, removendo os patches visuais legados substituídos em vez de acrescentar uma nova camada de correções sobre eles.

## Segurança
- snapshot da v1.6 arquivado em archive/index-v1.6.html;
- schemaVersion permanece 3;
- chave localStorage permanece minhafrequencia_v03;
- nenhuma migração de dados foi introduzida;
- nenhuma regra funcional de frequência, calendário, eventos ou programas foi alterada.

## Integração visual
- legenda do calendário substituída pelo componente aprovado no Gate 3;
- 11 categorias na legenda: presença, parcial, falta, sem aula, EaD, prova, seminário, atividade, entrega, institucional e feriado;
- presença e falta ganharam glyphs semânticos próprios, distintos do check/x genéricos de interface;
- estados equivalentes em calendário, histórico, ações de hoje e overlay de frequência usam a mesma família;
- botões, controles, chips, icon buttons, cards clicáveis, formulários, onboarding, sheets e bottom nav seguem os tokens aprovados;
- emojis continuam como conteúdo e não como controles estruturais.

## Limpeza CSS
- removidos integralmente os blocos visuais cumulativos v1.4.1, v1.4.2, v1.4.3, v1.5, v1.5.1 e v1.6;
- substituídos por um único bloco: v1.7 — Gate 6: design system integrado;
- aproximadamente 25 mil caracteres de patches visuais legados foram removidos;
- o CSS resultante mantém os estilos funcionais/base anteriores e uma única camada consolidada de design system.

## Tokens
- spacing: 4, 6, 8, 12, 16, 20, 24, 32 px;
- radius: 6, 8, 10, 12, 16, 20 px;
- chip: 36 px;
- touch target: 44 px;
- controle padrão: 48 px;
- stroke iconográfico: 1.75;
- cores semânticas ligadas aos tokens de verde, lavanda, coral, amarelo, turquesa e azul.

## Validações
- JavaScript completo validado com new Function: sem erro;
- tags style balanceadas;
- nenhum marcador dos antigos blocos visuais v1.4.1–v1.6 permanece no CSS;
- 11 chips da legenda presentes;
- referências de assets atualizadas para v1.7;
- cache PWA atualizado para minhafrequencia-v1.7.0.