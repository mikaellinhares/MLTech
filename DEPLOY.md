# 🚀 Guia de Deploy - MLTech

## ✅ Site Criado com Sucesso!

Seu site corporativo da MLTech foi criado com sucesso usando Astro e está pronto para deploy no GitHub Pages.

## 📋 O que foi criado:

### ✅ Páginas Completas:
- **Página Inicial** (`/`) - Hero section, serviços e estatísticas
- **Sobre** (`/sobre`) - História da empresa, valores e equipe
- **Serviços** (`/servicos`) - Desenvolvimento web, desktop e automações
- **Portfólio** (`/portfolio`) - Projetos com filtros por categoria
- **Contato** (`/contato`) - Formulário e informações de contato

### ✅ Recursos Implementados:
- Design moderno e responsivo com Tailwind CSS
- Navegação mobile com menu hambúrguer
- Formulário de contato funcional
- Filtros de portfólio interativos
- FAQ com accordion
- SEO otimizado
- Configuração para GitHub Pages

## 🚀 Próximos Passos para Deploy:

### 1. Configurar Repositório GitHub
```bash
# Se ainda não fez, inicialize o git
git init
git add .
git commit -m "Initial commit: MLTech website"

# Conecte ao seu repositório GitHub
git remote add origin https://github.com/SEUUSUARIO/MLTech.git
git push -u origin main
```

### 2. Atualizar Configurações
Edite o arquivo `astro.config.mjs`:
```javascript
export default defineConfig({
  site: 'https://SEUUSUARIO.github.io',  // Substitua SEUUSUARIO
  base: '/MLTech',                       // Substitua pelo nome do seu repo
  // ... resto da configuração
});
```

### 3. Habilitar GitHub Pages ⚠️ IMPORTANTE
1. Vá para **Settings** > **Pages** no seu repositório
2. Em **Source**, selecione **GitHub Actions** (NÃO use "Deploy from a branch")
3. Salve as configurações
4. **ESSENCIAL**: Se você ver a opção "Deploy from a branch" selecionada, o site NÃO funcionará. Você DEVE selecionar "GitHub Actions"

### 4. Deploy Automático
- Faça push para a branch `main`
- O GitHub Actions fará o deploy automaticamente
- Seu site estará disponível em: `https://SEUUSUARIO.github.io/MLTech`

## 🎨 Personalização Rápida:

### Alterar Informações da Empresa:
1. **Nome da empresa**: Edite em todos os arquivos `.astro`
2. **Contato**: Atualize em `src/components/Footer.astro` e `src/pages/contato.astro`
3. **Cores**: Modifique as classes Tailwind CSS (blue-600, green-600, etc.)

### Adicionar Imagens:
1. Coloque imagens na pasta `public/`
2. Referencie com `/nome-da-imagem.jpg`

### Adicionar Mais Projetos:
1. Edite o array `projects` em `src/pages/portfolio.astro`
2. Adicione novos objetos com as informações do projeto

## 🔧 Comandos Úteis:

```bash
# Desenvolvimento local
npm run dev

# Build para produção
npm run build

# Preview do build
npm run preview

# Verificar se tudo está funcionando
npm run build && npm run preview
```

## 📱 Teste Local:
O servidor de desenvolvimento está rodando em `http://localhost:4321`

## 🎯 Recursos do Site:

### Página Inicial:
- Hero section com call-to-action
- Cards de serviços principais
- Estatísticas da empresa
- Seção de call-to-action final

### Página Sobre:
- História da empresa
- Valores e missão
- Estatísticas em destaque
- Apresentação da equipe

### Página Serviços:
- Cards detalhados de cada serviço
- Preços estimados
- Processo de trabalho
- Serviços adicionais

### Página Portfólio:
- Grid de projetos com filtros
- Tecnologias utilizadas
- Depoimentos de clientes
- Estatísticas de resultados

### Página Contato:
- Formulário completo de contato
- Informações de contato
- Links para redes sociais
- FAQ com accordion

## 🚨 Importante:
- **Teste sempre localmente** antes de fazer deploy
- **Atualize as informações de contato** com dados reais
- **Adicione imagens reais** da empresa e projetos
- **Configure o domínio personalizado** se necessário

## 🎉 Parabéns!
Seu site corporativo está pronto e profissional. Boa sorte com seu negócio!

---
**MLTech** - Transformando ideias em soluções tecnológicas 🚀


