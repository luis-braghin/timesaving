# Time Saving Tech - Site Institucional

Site moderno e profissional para a Time Saving Tech, empresa de soluções em automação e inteligência artificial.

## 🚀 Deploy na Vercel (Recomendado)

### Opção 1: Deploy direto pelo GitHub

1. **Suba o código para o GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/seu-usuario/timesaving-site.git
   git push -u origin main
   ```

2. **Conecte na Vercel:**
   - Acesse [vercel.com](https://vercel.com) e faça login com GitHub
   - Clique em "Add New..." → "Project"
   - Selecione o repositório `timesaving-site`
   - A Vercel detecta automaticamente que é um projeto Vite
   - Clique em "Deploy"

3. **Configure o domínio:**
   - No dashboard do projeto, vá em "Settings" → "Domains"
   - Adicione `timesavingtech.com.br`
   - Siga as instruções para configurar o DNS no Registro.br

### Opção 2: Deploy via CLI

```bash
npm install -g vercel
vercel login
vercel --prod
```

## 💻 Desenvolvimento Local

```bash
# Instalar dependências
npm install

# Rodar em modo desenvolvimento
npm run dev

# Build para produção
npm run build

# Preview do build
npm run preview
```

## 📁 Estrutura do Projeto

```
timesaving-site/
├── public/
│   └── favicon.svg
├── src/
│   ├── App.jsx          # Componente principal com todas as seções
│   ├── index.css        # Estilos globais + Tailwind
│   └── main.jsx         # Entry point
├── index.html
├── package.json
├── tailwind.config.js
├── postcss.config.js
└── vite.config.js
```

## ✏️ Personalizações Comuns

### Adicionar novos clientes

No arquivo `src/App.jsx`, encontre o array `clients` na função `Clients()`:

```javascript
const clients = [
  {
    name: 'Escritório de Advocacia BBL',
    logo: null, // ou '/path/to/logo.png'
  },
  // Adicione novos clientes aqui:
  {
    name: 'Nova Empresa',
    logo: '/logos/nova-empresa.png', // coloque o logo em public/logos/
  },
]
```

### Alterar informações de contato

No componente `Contact()`, atualize:

```javascript
const whatsappNumber = '5519981250530' // Número do WhatsApp
const emailAddress = 'luis@timesavingtech.com.br' // E-mail de contato
```

### Alterar cores da marca

No arquivo `tailwind.config.js` e `src/index.css`, atualize as variáveis de cor:

```javascript
// tailwind.config.js
colors: {
  'ts-cyan': '#00d4ff',    // Cor principal
  'ts-purple': '#7c3aed',  // Cor secundária
}
```

### Adicionar logo

Substitua o ícone de relógio pelo logo:

1. Coloque o logo em `public/logo.png`
2. No `App.jsx`, importe e use a imagem no componente `Navigation` e `Footer`

## 🔧 Configuração do Formulário

O formulário de contato está preparado para integração. Opções recomendadas:

1. **Formspree** (mais simples):
   - Crie conta em [formspree.io](https://formspree.io)
   - Substitua o `handleSubmit` pelo action do Formspree

2. **EmailJS** (sem backend):
   - Configure em [emailjs.com](https://emailjs.com)
   - Receba e-mails diretamente no seu inbox

3. **Webhook para n8n** (para vocês que já usam):
   - Crie um webhook no n8n
   - Faça POST dos dados do formulário para o webhook

## 📱 Responsividade

O site é totalmente responsivo e otimizado para:
- Desktop (1280px+)
- Tablet (768px - 1279px)
- Mobile (< 768px)

## 🎨 Tecnologias

- **React 18** - Framework frontend
- **Vite** - Build tool ultrarrápido
- **Tailwind CSS** - Estilização utilitária
- **Lucide React** - Ícones modernos

---

Desenvolvido com ☕ para Time Saving Tech
