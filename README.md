# Case Tarumã Componentes — Delta Academy

Portal de materiais didáticos da **Certificação FDE** (Forward Deployed Engineer) da Delta Academy.

## O que é

Site estático que disponibiliza os materiais de estudo do curso de certificação FDE, incluindo:

- **Case Tarumã Componentes**: um case de estudo simulado sobre uma estamparia de Joinville que precisa resolver problemas na área de contas a pagar.
- **FDEPlay**: trilha de estudo com 9 materiais adicionais (vídeos, leituras e repositório) sobre o papel do Forward Deployed Engineer.
- **Aula Especial**: formulário de inscrição para eventos ao vivo, com integração a Google Apps Script.

## Funcionalidades

- Download de materiais em PDF e ZIP (caderno do aluno, relatos de campo, guia de preenchimento, kit do FDE, slides do hotseat)
- Marcação de progresso de leitura (persistida no `localStorage`)
- Seção de resolução protegida por senha com arquivos criptografados (AES-256-CBC via Web Crypto API)
- Filtro e busca de arquivos por categoria
- Navegação por abas nas etapas do kit do FDE
- Tema claro/escuro automático (segue `prefers-color-scheme`)
- Trilha FDEPlay com resumos passo a passo e marcação de materiais estudados
- Formulário de inscrição para aula especial com validação client-side e envio para Apps Script

## Stack Tecnológica

- **HTML5** + **CSS3** (variáveis CSS, grid, flexbox, media queries)
- **JavaScript** vanilla (ES5+ para compatibilidade)
- **Web Crypto API** para decriptação de arquivos protegidos
- **Google Apps Script** como backend do formulário de inscrição
- **GitHub Pages** para hospedagem (indicado pelo `.nojekyll`)

## Estrutura de Pastas

```
/
├── index.html              # Página principal do Case Tarumã
├── fdeplay.html            # Trilha de estudo FDEPlay
├── arquivos/               # PDFs e ZIPs dos materiais do case
├── miniaturas/             # Imagens de preview dos PDFs
├── marca/                  # Logotipos (SVG) da Delta Academy
├── restrito/               # Arquivos JS com PDFs criptografados (resolução)
├── aulaespecial/           # Formulário de inscrição para aula especial
│   ├── index.html          # Página de inscrição
│   ├── config.js           # URL do Apps Script (backend)
│   ├── estilo.css          # Estilos do formulário
│   └── arquivo/            # Área administrativa de inscrições
└── .nojekyll               # Desabilita processamento Jekyll no GitHub Pages
```

## Como Usar

1. Clone o repositório:
   ```bash
   git clone https://github.com/rodrigosilvacio/fde-delta.git
   ```

2. Abra `index.html` em um navegador para acessar o Case Tarumã Componentes.

3. Abra `fdeplay.html` para acessar a trilha de estudo FDEPlay.

4. Para o formulário de aula especial funcionar, é necessário configurar a URL do Apps Script em `aulaespecial/config.js`.

## Hospedagem

O site foi projetado para funcionar diretamente via GitHub Pages ou qualquer servidor de arquivos estáticos. Não há etapa de build.

## Variáveis de Ambiente

| Nome | Descrição |
|------|-----------|
| `AULA_ESPECIAL_API` | URL do Google Apps Script publicado como web app (configurada em `aulaespecial/config.js`) |

## Licença

Conteúdo didático da Delta Academy. Empresa, pessoas e números do case são fictícios.
