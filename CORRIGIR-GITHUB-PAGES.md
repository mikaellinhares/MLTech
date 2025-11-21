# 🚨 Como Corrigir o Erro do GitHub Pages

## Problema Atual

O GitHub Pages está tentando fazer deploy usando **Jekyll** (processador padrão), mas o projeto é **Astro**.

Erro exibido:
```
ERROR: YOUR SITE COULD NOT BE BUILT:
Invalid YAML front matter in /github/workspace/src/pages/portfolio/sistema-inventario-estoque.astro
```

---

## ✅ Solução (Siga EXATAMENTE estes passos)

### 1. Configurar GitHub Pages para usar GitHub Actions

1. Acesse seu repositório no GitHub: `https://github.com/mikaellinhares/MLTech`
2. Clique em **Settings** (Configurações)
3. No menu lateral esquerdo, clique em **Pages**
4. Na seção **"Source"** (Origem):
   - ❌ **NÃO use**: "Deploy from a branch"
   - ✅ **Selecione**: "GitHub Actions"
5. Clique em **Save** (Salvar)

### 2. Fazer Commit das Alterações

Execute estes comandos no terminal:

```bash
# Adicionar as alterações (incluindo o arquivo .nojekyll)
git add .

# Criar commit
git commit -m "fix: adiciona .nojekyll e corrige configuração para Astro"

# Enviar para GitHub
git push origin main
```

### 3. Verificar o Deploy

1. Acesse a aba **Actions** no seu repositório
2. Você deverá ver um novo workflow rodando: "Deploy to GitHub Pages"
3. Aguarde o workflow completar (leva 1-3 minutos)
4. Quando aparecer um ✅ verde, seu site estará no ar!

### 4. Acessar o Site

Após o deploy, acesse: `https://mikaellinhares.github.io/MLTech/`

---

## 🔍 O que foi corrigido no código?

### Arquivo `.nojekyll` adicionado
- **Localização**: `public/.nojekyll`
- **Propósito**: Desabilita o processamento Jekyll no GitHub Pages
- **Status**: ✅ Já criado

### Favicon com suporte ao base URL
- **Arquivo**: `src/layouts/Layout.astro`
- **Mudança**: Agora usa `import.meta.env.BASE_URL` para o caminho do favicon
- **Status**: ✅ Já corrigido

### Documentação atualizada
- **README.md**: Adicionada seção de troubleshooting
- **DEPLOY.md**: Instruções mais claras sobre GitHub Actions
- **Status**: ✅ Já atualizado

---

## ❓ Perguntas Frequentes

### Por que o erro aconteceu?

O GitHub Pages, por padrão, usa **Jekyll** para processar sites estáticos. Como nosso site é **Astro**, precisamos usar **GitHub Actions** para fazer o build correto.

### O que é o arquivo `.nojekyll`?

É um arquivo especial que informa ao GitHub Pages para NÃO usar o Jekyll. Ele deve estar na pasta `public/` para ser copiado para o build final.

### Como saber se está funcionando?

1. Na aba **Actions**, você verá o workflow "Deploy to GitHub Pages" executando
2. O workflow terá as etapas:
   - ✅ Checkout your repository using git
   - ✅ Install, build, and upload your site
   - ✅ Deploy to GitHub Pages
3. Quando todas tiverem ✅, o site estará no ar

---

## 📞 Ainda com problemas?

Se após seguir todos os passos o erro persistir:

1. Verifique se você realmente selecionou **"GitHub Actions"** em Settings > Pages
2. Tente fazer um novo push:
   ```bash
   git commit --allow-empty -m "trigger rebuild"
   git push origin main
   ```
3. Aguarde 2-3 minutos para o workflow completar

---

**Última atualização**: 2025-11-20
