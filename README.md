<!DOCTYPE html>
<html lang="pt-br">

  <head>
    <meta charset="UTF-8" />
    <meta name="DiegoFerreira" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" type="text/css" href="stylee.css">
    <title>DiegoFerreira</title>
  </head>

  <body load="onload()">
   <div class="center">
    <div class="ring"></div>
    <span>carregando...</span>
   </div>

  <!-- Agrupa os elementos que compõe o cabeçalho. -->
  <header>
    <a href="./layout.html" id="logo">Logo</a>

    <button id="openMenu">&#9776;</button>

    <!-- Agrupa links de navegação no site. -->
    <nav id="menu">

      <button id="closeMenu">X</button>

      <a href="#">Home</a>
      <a href="about.html">About me!</a>
      <a href="#">Products</a>
      <a href="">Contact</a>
    </nav>

  </header>

  <!-- Agrupa o conteúdo principal da página ou aplicação. -->
  <!-- Canvas 3D -->
  <!-- Outros conteúdos da seção -->
  <main id="canvas-main">
    <canvas id="canvas3d"></canvas>
  </main>
  <!-- Agrupa informações e links relacionado ao conteúdo principal. -->
  <aside>Aside</aside>

  <!-- Agrupa informações de autoria, direitos autorais, contato,
         mapa do site, links e documento relacionados. -->
  <footer>Footer</footer>
  
    <script type="module">
      import { Application } from './runtime.js';
      const canvas = document.getElementById('canvas3d');
      const app = new Application(canvas);
      app.load('./scene.splinecode');
    </script>

  <script>
    window.addEventListener('load', function() {
      // Seleciona o elemento .center
      const centerElement = document.querySelector('.center');

      // Adiciona a classe .center-hidden com um pequeno atraso
      setTimeout(function() {
        centerElement.style.opacity = '0';
        centerElement.style.visibility = 'hidden';
      }, 1000); // Tempo de atraso em milissegundos (aqui é 1 segundo)
    });
  </script>

  </body>
</html>
  
