# ⚡ MWServEnergy – Troca de Padrão de Entrada

[![Deploy](https://img.shields.io/badge/Deploy-GitHub%20Pages-blue?style=for-the-badge&logo=github)](https://washingtonton.github.io/washingtonTon-mwservenergy-troca-padrao/)
![Status](https://img.shields.io/badge/Status-Online-brightgreen?style=for-the-badge)
![Tech](https://img.shields.io/badge/Feito%20com-HTML%20%7C%20CSS%20%7C%20JS-orange?style=for-the-badge)

Projeto desenvolvido para apresentar os serviços da **MWServEnergy**, com foco em instalações elétricas, **troca de padrão de entrada** e **organização de quadros elétricos**.  
O site é publicado via **GitHub Pages** e utiliza um **arquivo JSON** para carregar imagens e métricas de forma dinâmica.

🔗 [👉 Acesse o site publicado aqui](https://washingtonton.github.io/washingtonTon-mwservenergy-troca-padrao/)

---

## 📂 Estrutura do Projeto

├── index.html # Página principal do site
├── style.css # Estilos visuais
├── script.js # Código JS que consome o data.json
├── data.json # Arquivo de dados (galeria + métricas)
├── gallery/ # Pasta de imagens utilizadas no site
│ ├── IMG-20190319-WA0024.jpg
│ ├── IMG_20210122_170611120.jpg
│ ├── IMG_20181121_151239572.jpg
│ ├── 20190615_163243.jpg
│ ├── 20190315_170541.jpg
│ ├── 20200215_211145.jpg
│ ├── IMG_20181121_151201222.jpg
│ ├── IMG_20181115_103511701.jpg
│ ├── IMG-20230803-WA0050.jpg


Copiar código

---

## 🖼️ Galeria de Imagens

As imagens do site não estão fixas no código HTML.  
Elas são carregadas automaticamente a partir do arquivo **`data.json`**, que organiza os caminhos e as legendas.

Exemplo dentro do `data.json`:

```json
{
  "src": "gallery/IMG-20190319-WA0024.jpg",
  "caption": "Barramentos e quadro organizado"
}
➕ Como adicionar novas imagens
Coloque a nova foto dentro da pasta gallery/

Abra o arquivo data.json e adicione um novo item dentro de "gallery":

json
Copiar código
{
  "src": "gallery/nome-da-imagem.jpg",
  "caption": "Descrição da foto"
}
Salve, faça commit e envie para o GitHub:

bash
Copiar código
git add .
git commit -m "Adicionando nova imagem à galeria"
git push origin main
Atualize a página publicada no GitHub Pages (Ctrl+F5 no navegador)

📊 Métricas do Projeto
Além das imagens, o data.json também armazena indicadores importantes, como:

Perdas elétricas antes e depois da correção

Número de equipamentos preservados

Economia média de kWh por mês

Essas métricas são exibidas automaticamente no site.

📞 Contato
📌 MWServEnergy – Washington
📱 WhatsApp: +55 11 92011-3230

🚀 Desenvolvido para apresentar profissionalmente os serviços de elétrica e projetos da MWServEnergy.
