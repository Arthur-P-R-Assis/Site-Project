<script>
export default {
  data() {
    return {
      imageUrl1: "https://raw.githubusercontent.com/Arthur-P-R-Assis/Site-Project/refs/heads/main/IMAGES/blusa-feminina.jpg",
      imageUrl2: "https://raw.githubusercontent.com/Arthur-P-R-Assis/Site-Project/refs/heads/main/IMAGES/istockphoto-173239968-612x612.jpg",
      imageUrl3: "https://raw.githubusercontent.com/Arthur-P-R-Assis/Site-Project/refs/heads/main/IMAGES/istockphoto-483960103-612x612.jpg",
      imageUrl4:"https://raw.githubusercontent.com/Arthur-P-R-Assis/Site-Project/refs/heads/main/IMAGES/istockphoto-1332758692-612x612.jpg",
      imageUrl5:"https://raw.githubusercontent.com/Arthur-P-R-Assis/Site-Project/refs/heads/main/IMAGES/71dSGi4xSvL.jpg",
      imageUrl6:"https://raw.githubusercontent.com/Arthur-P-R-Assis/Site-Project/refs/heads/main/IMAGES/23259012_01.jpg",
      menuAberto: false
    };
  },
  methods: {
    toggleMenu() {
      this.menuAberto = !this.menuAberto;
    }
  }
};
</script>

<template>
  <div class="container">
    <header>
      <div class="header-esquerdo">
        <button class="botao-lista" @click="toggleMenu">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-list" viewBox="0 0 16 16">
            <path fill-rule="evenodd" d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5m0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5m0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5"/>
          </svg>
        </button>
        <h1 class="titulo">LARISTORE</h1>
      </div>

      <div class="botoes">
        <button class="botao-carrinho">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-cart" viewBox="0 0 16 16">
            <path d="M0 1.5A.5.5 0 0 1 .5 1H2a.5.5 0 0 1 .485.379L2.89 3H14.5a.5.5 0 0 1 .491.592l-1.5 8A.5.5 0 0 1 13 12H4a.5.5 0 0 1-.491-.408L2.01 3.607 1.61 2H.5a.5.5 0 0 1-.5-.5M3.102 4l1.313 7h8.17l1.313-7zM5 12a2 2 0 1 0 0 4 2 2 0 0 0 0-4m7 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4m-7 1a1 1 0 1 1 0 2 1 1 0 0 1 0-2m7 0a1 1 0 1 1 0 2 1 1 0 0 1 0-2"/>
          </svg>
        </button>
        <button class="botao-perfil">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-person-circle" viewBox="0 0 16 16">
            <path d="M11 6a3 3 0 1 1-6 0 3 3 0 0 1 6 0"/>
            <path fill-rule="evenodd" d="M0 8a8 8 0 1 1 16 0A8 8 0 0 1 0 8m8-7a7 7 0 0 0-5.468 11.37C3.242 11.226 4.805 10 8 10s4.757 1.225 5.468 2.37A7 7 0 0 0 8 1"/>
          </svg>
        </button>
      </div>
    </header>
    
    <div v-if="menuAberto" class="menu">
      <ul>
        <li>Roupas Masculinas</li>
        <li>Roupas Femininas</li>
        <li>Tênis</li>
        <li>Acessórios</li>
        <li>Promoções</li>
      </ul>
    </div>

    <main>
      <div class="roupas-cima">
        <div class="roupa-item">
          <img :src="imageUrl1" alt="Blusa Feminina" class="roupass"/>
          <p class="nome-imagem">Blusa Feminina</p>
          <p class="nome-imagem">R$34,90</p>
        </div>
        <div class="roupa-item">
          <img :src="imageUrl3" alt="Camisa Preta" class="roupass"/>
          <p class="nome-imagem">Camisa Preta</p>
          <p class="nome-imagem">R$29,90</p>
        </div>
        <div class="roupa-item">
          <img :src="imageUrl2" alt="Calça Jeans" class="roupass"/>
          <p class="nome-imagem">Calça Jeans</p>
          <p class="nome-imagem">R$119,90</p>
        </div>
      </div>
      <div class="roupas-baixo">
        <div class="roupa-item">
          <img :src="imageUrl6" alt="Salto Alto" class="roupass"/>
          <p class="nome-imagem">Salto Alto</p>
          <p class="nome-imagem">R$229,90</p>
        </div>
        <div class="roupa-item">
          <img :src="imageUrl5" alt="Tênis" class="roupass" />
          <p class="nome-imagem">Tênis</p>
          <p class="nome-imagem">R$144,90</p>
        </div>
        <div class="roupa-item">
          <img :src="imageUrl4" alt="Short" class="roupass"/>
          <p class="nome-imagem">Short</p>
          <p class="nome-imagem">R$44,90</p>
        </div>

      </div>
    </main>

    <footer>
      <h4 class="telefone">Telefone: 27998416531</h4>
      <div class="endereco">
        <h5>Rua Desembargador Homero Mafra, 60 - Enseada do Suá</h5>
        <h5>Vitória - ES, 29050-275</h5>
      </div>
    </footer>
  </div>
</template>

<style>
  body {
    margin: 0px;
    padding: 0px;
    overflow-x: hidden;
  }

  main{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    gap: 20px;
  }

  .roupas-cima{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    text-align: center;
    gap:20px;
  }

  .roupas-baixo{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    text-align: center;
    gap:20px;
  }

  .roupass{
    border: 2px solid black;
    border-radius: 8px;
  }

  .nome-imagem {
    font-size: 14px;
    color: #333;
    text-decoration: underline;
    cursor: pointer;
    margin-top: 8px;
    font-weight: bold;
  }

  .roupa-item:hover{
    transform: scale(1.15);
    cursor:pointer;
  }

  img {
  width: 150px;
  height: 150px; 
  }

  .container{
    display:flex;
    flex-direction: column;
    justify-content: space-between;
    background-color: whitesmoke;
    width: 100%;
    height: 100vh;
    margin:0px;
    padding:0px;
    padding-top: 0px;
    align-items: center;
  }

  header{
    display:flex;
    flex-direction: row;
    justify-content: space-between;
    width:100%;
    margin: 0px;
    padding: 0px;
    color: white;
    background-color: black;
    display:flex;
    align-items: center;
    border-bottom: 4px solid #ccc;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    background-image: linear-gradient(to bottom, black, black 90%, #666 100%);
  }

  .header-esquerdo{
    display: flex;
    flex-direction: row;
    gap: 20px;
    justify-content: space-between;
    align-items: center;
  }

  .botoes{
    display: flex;
    margin-right: 30px;
    gap: 10px;
  }

  .botao-lista{
    border:none;
    background-color: black;
    cursor: pointer;
  }

  .botao-lista:hover{
    transform: scale(1.05);
  }

  .bi-list{
    width: 40px;
    height: 40px;
    fill:white;
  }

  .botao-carrinho{
    border:none;
    background-color: black;
    cursor: pointer;
  }
  .botao-carrinho:hover{
    transform: scale(1.15);
  }
  .bi-cart{
    width: 25px;
    height: 25px;
    fill:white;
  }

  .botao-perfil{
    border:none;
    background-color: black;
    cursor: pointer;
  }

  .botao-perfil:hover{
    transform: scale(1.15);
  }

  .bi-person-circle{
    width: 25px;
    height: 25px;
    fill:white;
  }

  footer{
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 0px;
    margin: 0;
    border-top: 4px solid #ccc;
  }

  footer h5,
  footer h6,
  footer h4 {
    margin: 2px 0;
    padding: 0;
    font-weight: bold;
    text-align: center;
  }

  .endereco{
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 2px;
    margin-bottom: 10px;
  }

  .menu {
    width: 100%;
    background-color: black;
    color: white;
    position: absolute;
    top: 80px; 
    left: 0;
    height: 100%;
    width: 30%; 
    display: flex;
    justify-content: top;
    align-items: center;
    flex-direction: column; 
  }

  .menu ul {
    list-style-type: none;
    padding: 0;
    width: 100%;
    display: flex;
    flex-direction: column; /* Alinha os itens na vertical */
    align-items: center;
  }

  .menu ul li {
    padding-top: 20px;
    padding-bottom: 20px;
    text-align: center;
    width: 100%;
    border-bottom: 1px solid white; /* Para separação entre os itens */
  }

  .menu ul li:hover{
    transform: scale(1.05);
  }

  .menu ul li:hover {
    background-color: #444;
    cursor: pointer;
  }
</style>
