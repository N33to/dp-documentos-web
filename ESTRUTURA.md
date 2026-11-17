# Estrutura do projeto

Mapa das pastas e arquivos de código. O código-fonte não é publicado neste repositório
(é software de uso interno de uma empresa real); aqui fica a arquitetura.

```text
├── ocr/   # motor de OCR e classificação (Python + Tesseract)
│   ├── tests/
│   │   ├── conferir_tela.py
│   │   └── test_classificar.py
│   ├── web/
│   │   ├── app.css
│   │   ├── app.js
│   │   └── index.html
│   ├── classificar.py
│   ├── diagnostico.py
│   ├── ocr.py
│   ├── ocr_lote.py
│   ├── organizar.py
│   ├── servidor.py
│   └── ver_paginas.py
└── web/   # site PHP: cadastro, dossiê de documentos, documentação de obra, acessos
    ├── app/
    │   ├── modulos/
    │   │   ├── acesso/
    │   │   │   ├── Api.php
    │   │   │   └── Central.php
    │   │   ├── colaboradores/
    │   │   │   ├── Alertas.php
    │   │   │   ├── Api.php
    │   │   │   └── Cadastro.php
    │   │   ├── dossie/
    │   │   │   ├── Api.php
    │   │   │   ├── Dossie.php
    │   │   │   ├── Importador.php
    │   │   │   └── Tipos.php
    │   │   ├── empresas/
    │   │   │   ├── Api.php
    │   │   │   └── Empresas.php
    │   │   └── obras/
    │   │       ├── Api.php
    │   │       ├── Catalogo.php
    │   │       └── Documentos.php
    │   ├── nucleo/
    │   │   ├── Acesso.php
    │   │   ├── Api.php
    │   │   ├── Auditoria.php
    │   │   ├── Banco.php
    │   │   ├── Config.php
    │   │   ├── ErroDeApi.php
    │   │   ├── Pdf.php
    │   │   ├── Permissao.php
    │   │   ├── Recurso.php
    │   │   ├── Requisicao.php
    │   │   ├── Seguranca.php
    │   │   ├── Senha.php
    │   │   ├── Sessao.php
    │   │   ├── Tentativas.php
    │   │   ├── Util.php
    │   │   └── Xlsx.php
    │   ├── bootstrap.php
    │   ├── config.local.exemplo.php
    │   └── config.php
    ├── public/
    │   ├── assets/
    │   │   ├── css/
    │   │   │   ├── app.css
    │   │   │   └── tema.css
    │   │   └── js/
    │   │       ├── acessos.js
    │   │       ├── app.js
    │   │       ├── colaboradores.js
    │   │       ├── confirmacoes.js
    │   │       ├── dossie.js
    │   │       ├── empresas.js
    │   │       └── obras.js
    │   ├── api.php
    │   ├── raiz.exemplo.php
    │   └── sistema.php
    ├── scripts/
    │   ├── importar_organizador.php
    │   ├── instalar.php
    │   ├── mariadb_local.ps1
    │   ├── servidor_local.ps1
    │   └── sincronizar_organizador.php
    ├── sql/
    │   └── esquema.sql
    └── tests/
        ├── conferir_tela.js
        ├── config.teste.php
        ├── fumaca_api.py
        ├── rodar.php
        └── semear_demo.php
```

## Tamanho (linhas, sem bibliotecas de terceiros)

| Linguagem | Linhas |
|---|---:|
| PHP | 7.323 |
| JavaScript | 3.325 |
| CSS | 2.055 |
| Python | 1.747 |
| SQL | 308 |
| HTML | 62 |
| PowerShell | 12 |

_Arquivos: 68._
