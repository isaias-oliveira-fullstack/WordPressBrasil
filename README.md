# 🔍 WordPress Brasil - Chrome Extension

Extensão para Google Chrome desenvolvida para otimizar a experiência de busca dentro do grupo WordPress Brasil no Facebook, permitindo que o usuário realize pesquisas de forma rápida, prática e centralizada através de um popup leve integrado ao navegador.

A extensão atua como um atalho inteligente para a funcionalidade de busca do próprio grupo, eliminando a necessidade de navegação manual até o Facebook, abertura do grupo e utilização da barra de pesquisa interna. Com apenas um clique no ícone da extensão, o usuário acessa um campo de pesquisa simples e direto, digita o termo desejado e é automaticamente redirecionado para a página de resultados filtrados dentro do grupo.

---

## 🚀 Sobre o projeto

Esta extensão foi desenvolvida para facilitar a busca de conteúdos dentro do grupo WordPress Brasil no Facebook, eliminando a necessidade de acessar manualmente o grupo e utilizar a barra de pesquisa interna.

Com um clique no ícone da extensão, o usuário pode:

- Digitar uma pesquisa
- Pressionar Enter ou clicar em "Pesquisar"
- Ser redirecionado diretamente para os resultados no grupo

---

## 🎯 Funcionalidade principal

- Campo de busca integrado ao popup da extensão
- Redirecionamento automático para o grupo WordPress Brasil no Facebook
- Suporte a pesquisa via Enter ou clique no botão
- Interface simples e leve

---

## 🧠 Problema que resolve

Antes da extensão:

- Abrir o Facebook
- Entrar no grupo manualmente
- Usar a busca interna

Depois da extensão:

✔ Clique na extensão  
✔ Digite a busca  
✔ Acesse os resultados diretamente  

---

## ⚙️ Tecnologias utilizadas

- HTML5
- CSS3
- JavaScript
- jQuery 1.9.1
- Chrome Extensions API (Manifest V2)

---

## 📂 Estrutura do projeto
```bash
WordPressBrasil/
│
├── WordPressBrasil/
│	│
│	├── css/
│	│   └── popup.css
│	│
│	├── img/
│	│   ├── 16.png
│	│   ├── 48.png
│	│   └── 128.png
│	│
│	├── js/
│	│   ├── jquery-1.9.1.min.js
│	│   └── popup.js
│	│
│	├── manifest.json
│	└── popup.html
│
├── LICENSE
├── README.md
├── UserGuide.md
└── WordPressBrasil.crx
```
---

## 🧩 Como funciona

function busca(){
    var itens = $("#buscar-item").val();

    if(itens){
        chrome.tabs.create({
            url: "https://www.facebook.com/groups/wordpress.brasil/search/?query=" + encodeURI(itens.toLowerCase())
        });
    }
}

$(document).ready(function(){

    $("input").focus();

    $("#buscar-item").keyup(function(e){
        if(e.which == 13){
            busca();
        }
    });

    $("#buscar-acao").click(function(){
        busca();
    });

});

Fluxo da aplicação:

1. Usuário digita o termo de busca  
2. Extensão captura o valor do input  
3. Monta URL de pesquisa do grupo  
4. Abre nova aba com os resultados  

---

## ⚡ Eventos da interface

- Enter no campo de busca → executa pesquisa  
- Clique no botão → executa pesquisa  
- Foco automático no input ao abrir popup  

---

## 📦 Instalação

1. Abrir: chrome://extensions/
2. Ativar modo desenvolvedor
3. Clicar em “Carregar sem compactação”
4. Selecionar a pasta do projeto

---

## 📘 Guia do Usuário

👉 Acesse o guia completo de uso e instalação da extensão:

🔗 [Abrir UserGuide.md](./UserGuide.md)

---

## 💡 Diferencial do projeto

- Extensão leve e direta  
- Foco em produtividade  
- Busca rápida em grupo do Facebook  
- Interface minimalista  

---

## 📌 Observações técnicas

- Manifest V2  
- jQuery 1.9.1  
- chrome.tabs.create para abrir resultados  

---

## 📄 Licença

Este projeto está licenciado sob a **Licença MIT**.

Veja o arquivo **[LICENSE](./LICENSE)** para mais detalhes. 

---

## 👨 Autor

Projeto desenvolvido por **Isaias Oliveira**.  
Conecte-se comigo no **[in/isaias-oliveira-dev](https://www.linkedin.com/in/isaias-oliveira-dev/)**
