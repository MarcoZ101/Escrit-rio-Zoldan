# Escritório Contábil Zoldan

Site do Escritório Contábil Zoldan — landing page de uma página só, em
HTML/CSS/JS puro (sem build, sem dependências).

## Estrutura

```
index.html   -> conteúdo e textos do site
styles.css   -> cores, fontes e layout (mexa em :root no topo para trocar as cores)
script.js    -> menu mobile e ano automático no rodapé
assets/      -> coloque aqui logo, favicon e fotos
```

## Checklist de personalização

- [x] Nome do escritório: "Escritório Contábil Zoldan"
- [x] WhatsApp/telefone: (49) 3353-4780
- [x] Instagram: @escritoriocontabilzoldan
- [x] E-mail: azcontabeis@azcontabeis.com.br
- [x] Endereço: Trav. Independência, 41, 1º andar sala 01, Centro, Xaxim/SC, CEP 89.825-000
- [x] Cores da marca (azul da logo) em `styles.css`, bloco `:root`
- [x] Textos de Serviços (11 serviços) e Sobre com conteúdo real
- [ ] Logo: enviar o **arquivo de imagem** da logo (PNG/SVG) para colocar em `assets/logo.png`
      e descomentar a tag `<img class="logo__img">` no `index.html` — por enquanto o
      cabeçalho usa texto estilizado com as cores da marca
- [ ] Confirmar horário de atendimento (está marcado como "a confirmar" no site)
- [ ] Depoimentos: ainda são exemplos — trocar por relatos reais de clientes quando tiver
- [ ] Fotos reais da equipe/escritório (seção Sobre)

## Como ver localmente

Não precisa instalar nada. Basta abrir o `index.html` no navegador,
ou rodar um servidor simples:

```bash
python3 -m http.server 8000
# depois acesse http://localhost:8000
```

## Como publicar (grátis)

Qualquer uma dessas opções funciona bem para este site estático:

### Opção A — Vercel (recomendado, mais simples)
1. Crie conta em vercel.com com o GitHub
2. "Add New Project" → selecione este repositório
3. Deploy automático a cada `git push`
4. Em "Settings → Domains", adicione seu domínio próprio e siga as instruções de DNS

### Opção B — Netlify
1. Crie conta em netlify.com com o GitHub
2. "Add new site → Import an existing project" → selecione este repositório
3. Build command: (vazio) — Publish directory: `/`
4. Em "Domain settings", adicione seu domínio próprio

### Opção C — GitHub Pages
1. No repositório, vá em Settings → Pages
2. Source: branch `main`, pasta `/ (root)`
3. Em "Custom domain", informe seu domínio e configure o DNS conforme a documentação do GitHub Pages

## Conectando o domínio que vocês já têm

No painel do registrador do domínio (Registro.br, HostGator, etc.), você vai
criar registros DNS apontando para o serviço escolhido acima. Cada serviço
(Vercel/Netlify/GitHub Pages) mostra exatamente quais registros CNAME/A criar
assim que você adiciona o domínio nas configurações dele.

## WhatsApp Business

- Baixe o app "WhatsApp Business" (diferente do WhatsApp comum)
- Configure: nome do escritório, categoria "Contabilidade", horário de atendimento,
  mensagem de saudação automática e mensagem de ausência
- O botão do site já usa o link `https://wa.me/55DDDNUMERO` — é só trocar o número

## Instagram

- Use conta comercial (Business), vinculada ao WhatsApp Business se possível
- Bio com link do site (uma boa opção é usar o link direto do site, já que é uma
  página só)
- Ideia de linha editorial inicial: dicas rápidas de prazos fiscais, mitos sobre
  MEI/Simples Nacional, bastidores do escritório, depoimentos de clientes
