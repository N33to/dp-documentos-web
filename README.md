# DP Web: dossiê de documentos por colaborador

Site de departamento pessoal que guarda a pasta de documentos de cada colaborador e controla o que cada construtora exige para liberar a equipe em obra. Acompanha um motor de OCR que separa e classifica PDFs escaneados.

> Protótipo de uso local. **O código e os dados não são públicos** (há documentos pessoais): este repositório traz a arquitetura em [ESTRUTURA.md](ESTRUTURA.md).

## O que faz

- **Dossiê:** pasta de documentos por pessoa, com checklist por tipo de documento e farol de pendências.
- **Documentação de obra:** construtora → obras → equipe → documentos exigidos de cada colaborador.
- **Organizador (Python + OCR):** recebe um PDF escaneado grande por pessoa, separa por documento e classifica pelo tipo; o que não reconhece vai para "a conferir", sem chute.
- **Acessos:** perfis e permissões por módulo, auditoria de ações.

## Decisões de engenharia

- **PHP 8.2+ e MySQL, sem Composer**, no mesmo desenho do [ERP](https://github.com/N33to/erp-gestao-empresarial).
- **Documento sai por link de uso único**, válido por 60 segundos; os arquivos nunca ficam na pasta pública.
- **Nada é apagado:** itens saem de uso, arquivo trocado continua em disco, ações vão para a auditoria.
- **OCR 100% local** (Tesseract): os PDFs têm dados pessoais e de saúde, então nada vai para API de terceiros. A pasta de origem é somente leitura.
- **Classificação em camadas**, da mais barata para a mais cara: correção manual, título, similaridade (TF-IDF), continuação do documento, frase do corpo, e só então revisão humana.
- **Testes com dados fictícios.** Nome real de pessoa só existe no banco de desenvolvimento.

## Stack

PHP 8.2+ · MySQL/MariaDB · JavaScript · HTML · CSS · Python · Tesseract (OCR) · Git
