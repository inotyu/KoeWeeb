# 📚 KoeWeeb - Leitor de Mangás Online

**🌐 [Acesse o site agora: **koeweeb.vercel.app**](https://koeweeb.vercel.app/)**

Plataforma moderna de leitura de mangás online com scraping inteligente e interface responsiva.

## 📋 Sumário

- [Visão Geral](#-visão-geral)
- [Funcionalidades](#-funcionalidades)
- [Tecnologias](#-tecnologias)
- [Instalação](#-instalação)
- [Configuração](#-configuração)
- [Estrutura](#-estrutura)
- [API Endpoints](#-api-endpoints)
- [Deploy](#-deploy)
- [Contribuição](#-contribuição)

## 🎯 Visão Geral

KoeWeeb é uma plataforma completa para leitura de mangás online que oferece:

- **Scraping Inteligente**: Coleta automática de múltiplas fontes
- **Interface Moderna**: Design responsivo e intuitivo
- **Leitor Avançado**: Navegação fluida entre capítulos
- **Busca Inteligente**: Encontre seus mangás favoritos facilmente
- **Categorias**: Navegue por gêneros e temas
- **Performance**: Otimizado para rápida carregamento

## ✨ Funcionalidades

### 📖 Leitor de Mangás
- 🖼️ **Visualização de alta qualidade** com zoom suave
- ⌨️ **Navegação por teclado** (setas, F para tela cheia)
- 📱 **Design responsivo** para todos os dispositivos
- 🔄 **Carregamento progressivo** de imagens

### 🔍 Busca e Descoberta
- 🔎 **Busca instantânea** de mangás
- 🏷️ **Filtragem por gêneros** (Romance, Drama, etc.)
- 📊 **Paginação inteligente** com lazy loading
- 🌟 **Mangás em destaque** na página inicial

### 🎨 Interface Moderna
- 🌙 **Tema escuro elegante** com acentos vermelhos
- ✨ **Animações suaves** e transições fluidas
- 📱 **Layout adaptativo** para mobile/desktop
- ⚡ **Performance otimizada**

## 🛠 Tecnologias

### Backend
- **Flask**: Framework web Python
- **BeautifulSoup4**: Parsing HTML
- **Requests**: HTTP client
- **Deep Translator**: Tradução automática

### Frontend
- **HTML5**: Semântico e moderno
- **CSS3**: Flexbox, Grid, Animations
- **JavaScript Vanilla**: Sem dependências
- **Inter**: Tipografia moderna

### Deploy
- **Vercel**: Serverless deployment
- **Python Runtime**: Ambiente de execução

## 🚀 Instalação

### 1. Clonar o repositório
```bash
git clone https://github.com/inotyu/koeweeb.git
cd koeweeb
```

### 2. Ambiente Virtual
```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

### 3. Dependências
```bash
pip install -r requirements.txt
```

### 4. Executar Localmente
```bash
python app.py
```

Acesse: http://localhost:5000

## ⚙️ Configuração

### Variáveis de Ambiente
Crie `.env.local` (opcional):
```env
# Configurações do scraper
SCRAPER_DELAY=1
MAX_RETRIES=3
TIMEOUT=10

# Cache (opcional)
CACHE_DURATION=300
```

### Configuração do Vercel
O projeto já está configurado para deploy no Vercel com `vercel.json`.

## 📁 Estrutura do Projeto

```
koeweeb/
├── app.py                 # Aplicação Flask principal
├── requirements.txt        # Dependências Python
├── vercel.json           # Configuração Vercel
├── routes/               # Blueprints Flask
│   ├── home.py           # Página inicial
│   ├── manga.py          # Detalhes do mangá
│   ├── ler.py            # Leitor de capítulos
│   ├── search.py         # Busca
│   └── genero.py         # Filtragem por gênero
├── scraper/              # Módulos de scraping
│   ├── base.py           # Configurações base
│   ├── mangas.py         # Scraping de mangás
│   ├── genres.py         # Lista de gêneros
│   ├── manga_info.py     # Detalhes do mangá
│   └── chapters.py       # Capítulos
├── templates/            # Templates Jinja2
│   ├── index.html        # Página inicial
│   ├── manga.html        # Página do mangá
│   ├── chapter.html      # Leitor
│   ├── search.html       # Busca
│   └── generos.html      # Gêneros
├── static/               # Arquivos estáticos
│   ├── css/              # Estilos
│   │   ├── index.css
│   │   ├── manga.css
│   │   ├── chapter.css
│   │   └── generos.css
│   └── script/           # JavaScript
│       ├── index.js
│       └── chapter.js
└── README.md             # Documentação
```

## 🔌 API Endpoints

### Páginas
- `GET /` - Página inicial com mangás recentes
- `GET /manga/<slug>` - Detalhes do mangá
- `GET /ler?url=<chapter_url>` - Leitor de capítulos
- `GET /search?q=<query>` - Busca de mangás
- `GET /genero/<genre_path>` - Mangás por gênero

### Funcionalidades
- **Scraping automático** de múltiplas fontes
- **Tradução automática** de sinopses
- **Cache inteligente** para performance
- **Tratamento de erros** robusto

## 🚀 Deploy

### Vercel (Recomendado)
```bash
# Instalar Vercel CLI
npm i -g vercel

# Deploy
vercel --prod
```

### Heroku
```bash
heroku create koeweeb
git push heroku main
```

### Railway/Render
Conecte o repositório e configure as variáveis de ambiente.

## 🤝 Contribuição

1. Fork o projeto
2. Crie branch: `git checkout -b feature/nova-funcionalidade`
3. Commit: `git commit -m 'Add nova funcionalidade'`
4. Push: `git push origin feature/nova-funcionalidade`
5. Pull Request

### Diretrizes
- **Python**: PEP 8, type hints quando possível
- **JavaScript**: ES6+, semântico
- **CSS**: BEM methodology, mobile-first
- **Commits**: Conventional Commits

## 📝 Licença

Este projeto está licenciado sob a Licença MIT.

## 🚨 Aviso Legal

Este projeto é para fins educacionais. Os usuários devem respeitar os termos de serviço das fontes de mangás e apoiar os criadores oficiais quando possível.

## 📞 Suporte

- **Issues**: [GitHub Issues](https://github.com/inotyu/koeweeb/issues)
- **Discord**: [Servidor Discord](https://discord.gg/koeweeb)

---

**Desenvolvido com ❤️ para a comunidade de leitores**
