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
- [x] E-mail: azcontabeis@azcontabeis.com.br (temporário — avisar quando tiver o novo)
- [x] Endereço: Trav. Independência, 41, 1º andar sala 01, Centro, Xaxim/SC, CEP 89.825-000
- [x] Horário de atendimento: Segunda a sexta, 7h45 às 18h
- [x] Textos de Serviços (11 serviços) e Sobre com conteúdo real
- [x] Seção de depoimentos removida a pedido do cliente
- [x] **Rebrand 2026 aplicado** (extraído do pacote do Claude Design): nova logo
      (símbolo de águia), paleta azul-marinho/azul, tipografia Roboto + Montserrat,
      novo layout de seções (hero escuro, faixa de estatísticas, pilares, split
      feature, banner de CTA) — ver `assets/logo-white.png`, `assets/eagle-mark.png`
- [ ] Fotos reais da equipe/escritório (seção Sobre e Hero — hoje usa imagens
      ilustrativas geradas no Claude Design)
- [ ] Estatísticas de prova social do rascunho original (anos de atuação, nº de
      clientes, tempo médio de resposta) foram **removidas** por não serem
      confirmadas — usamos só o que já sabíamos (16 anos desde 2010, CRC ativo)
- [ ] Tabela de preços e formulário de contato do rascunho **não foram incluídos**
      a pedido do cliente — contato continua só por WhatsApp
- [ ] "Área do cliente" (portal com login) é uma ideia do design para o futuro —
      não foi construída, pois depende de um sistema por trás (autenticação,
      armazenamento de documentos) que ainda não existe

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

## Conectando o domínio zoldancontabilidade.cnt.br (Vercel)

Domínio `.cnt.br` é registrado pelo Registro.br (categoria profissional de
contabilistas). O DNS dele se gerencia no mesmo painel de qualquer domínio
`.br`: registro.br → login → "Meus domínios" → `zoldancontabilidade.cnt.br`
→ "Editar Zona DNS" (ou "DNS").

Passo a passo:

1. Na Vercel, dentro do projeto → **Settings → Domains**, digite
   `zoldancontabilidade.cnt.br` e clique em "Add"
2. Repita para `www.zoldancontabilidade.cnt.br` (a Vercel geralmente já
   sugere isso automaticamente e faz o redirecionamento entre as duas versões)
3. A Vercel vai mostrar os registros exatos a criar — normalmente:
   - Domínio raiz (`zoldancontabilidade.cnt.br`): registro **A** apontando
     para `76.76.21.21`
   - Subdomínio `www`: registro **CNAME** apontando para `cname.vercel-dns.com`
4. No Registro.br, na Zona DNS do domínio, crie exatamente esses registros
   (copie os valores que a Vercel mostrar na hora, eles podem mudar)
5. Aguarde a propagação (minutos a poucas horas) — a Vercel marca o domínio
   como "Valid Configuration" quando terminar

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
