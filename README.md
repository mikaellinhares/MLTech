# MLTech - Portfólio

Site portfólio da MLTech desenvolvido com Astro e TailwindCSS.

## 🚀 Deploy no GitHub Pages

### Configuração Automática (Recomendado)

1. **Configure o GitHub Pages no repositório:**
   - Vá para Settings > Pages
   - ⚠️ **IMPORTANTE**: Em "Source", selecione **"GitHub Actions"**
   - NÃO selecione "Deploy from a branch" (isso usará Jekyll e causará erro)
   - Branch: main

2. **Push para o repositório:**
   ```bash
   git add .
   git commit -m "Deploy inicial"
   git push origin main
   ```

3. **O deploy será automático!** 
   - Acesse: `https://mikaellinhares.github.io/MLTech`

### Deploy Manual (Alternativo)

1. **Build do projeto:**
   ```bash
   npm run build
   ```

2. **Deploy para GitHub Pages:**
   ```bash
   npm run deploy
   ```

## 🛠️ Desenvolvimento Local

```bash
# Instalar dependências
npm install

# Executar em modo desenvolvimento
npm run dev

# Build para produção
npm run build

# Preview do build
npm run preview
```

## 📁 Estrutura do Projeto

```
src/
├── components/     # Componentes reutilizáveis
├── layouts/        # Layouts das páginas
├── pages/          # Páginas do site
│   ├── portfolio/  # Páginas individuais dos projetos
│   └── ...
└── styles/         # Estilos globais
```

## 🌐 URLs do Site

- **Home:** `https://mikaellinhares.github.io/MLTech/`
- **Portfólio:** `https://mikaellinhares.github.io/MLTech/portfolio`
- **Contato:** `https://mikaellinhares.github.io/MLTech/contato`
- **Serviços:** `https://mikaellinhares.github.io/MLTech/servicos`
- **Sobre:** `https://mikaellinhares.github.io/MLTech/sobre`

## 📱 Projetos do Portfólio

1. **Sistema de Inventário de Estoque**
   - URL: `/portfolio/sistema-inventario-estoque`
   - Tecnologias: Python, Flask, Pandas, SQLAlchemy

2. **Automação de Crédito Imobiliário**
   - URL: `/portfolio/automacao-credito-imobiliario`
   - Tecnologias: Python, Flask, Selenium

3. **Integração Magazord x Posthaus**
   - URL: `/portfolio/integracao-magazord-posthaus`
   - Tecnologias: Python, Flask, Cron Jobs, FTP, API REST

## 🔧 Tecnologias Utilizadas

- **Astro** - Framework para sites estáticos
- **TailwindCSS** - Framework CSS utilitário
- **GitHub Pages** - Hospedagem estática
- **GitHub Actions** - Deploy automático

## 🚨 Troubleshooting

### Erro: "Invalid YAML front matter" ou "jekyll-build-pages"

**Problema**: O GitHub Pages está tentando usar Jekyll ao invés de Astro.

**Solução**:
1. Vá para **Settings** > **Pages** no seu repositório
2. Em **Source**, mude de "Deploy from a branch" para **"GitHub Actions"**
3. Salve e faça um novo commit/push
4. O arquivo `.nojekyll` na pasta `public/` garante que Jekyll não seja usado

### Erro: Links não funcionam ou página em branco

**Problema**: Configuração incorreta do `base` no `astro.config.mjs`.

**Solução**:
- Verifique se `base: '/MLTech'` está configurado corretamente
- O nome deve corresponder ao nome do seu repositório GitHub