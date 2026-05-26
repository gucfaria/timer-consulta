# Timer de Consulta — PWA

Timer por fases para consultas psiquiátricas, instalável como app no celular.

## Estrutura de arquivos

```
/
├── index.html        ← app principal
├── manifest.json     ← configuração PWA
├── sw.js             ← service worker (cache offline)
└── icons/
    ├── icon-192.png
    └── icon-512.png
```

## Deploy no GitHub Pages (passo a passo)

### 1. Criar repositório

1. Acesse [github.com](https://github.com) e faça login
2. Clique em **New repository**
3. Nome sugerido: `timer-consulta`
4. Deixe **Public** (obrigatório para GitHub Pages gratuito)
5. Clique em **Create repository**

### 2. Fazer upload dos arquivos

**Opção A — pela interface web (mais simples):**
1. Na página do repositório, clique em **uploading an existing file**
2. Arraste todos os arquivos desta pasta (incluindo a pasta `icons/`)
3. Clique em **Commit changes**

**Opção B — via Git (linha de comando):**
```bash
git init
git add .
git commit -m "Timer de Consulta PWA"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/timer-consulta.git
git push -u origin main
```

### 3. Ativar GitHub Pages

1. No repositório, vá em **Settings → Pages**
2. Em *Source*, selecione **Deploy from a branch**
3. Branch: **main** / Folder: **/ (root)**
4. Clique em **Save**
5. Aguarde ~1 minuto. O app estará disponível em:
   `https://SEU_USUARIO.github.io/timer-consulta/`

### 4. Instalar no iPhone / Android

**iPhone (Safari):**
1. Abra o link no Safari
2. Toque em **Compartilhar** (ícone de caixa com seta)
3. Role e toque em **Adicionar à Tela de Início**
4. Confirme o nome e toque em **Adicionar**

**Android (Chrome):**
1. Abra o link no Chrome
2. Toque no menu ⋮ → **Adicionar à tela inicial**
3. Ou aguarde o banner automático de instalação

---

## Funcionalidades

- **Timer por fases** com cores, sons e flash visual nas transições
- **Visual tipo Time Timer**: arco que diminui conforme o tempo passa
- **Slider circular**: arraste a bolinha para ajustar o ponto da consulta
- **Wake Lock**: mantém a tela do celular acesa enquanto o timer está rodando
- **Offline**: funciona sem internet após a primeira visita
- **Janela popup**: botão ⧉ abre em janela flutuante separada (desktop)
- **Sincronização**: janela principal e popup se sincronizam em tempo real
