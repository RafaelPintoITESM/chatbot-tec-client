
<script lang="ts">
    import {
        Carousel
    } from 'flowbite-svelte';
        
      let images = [
          {
              alt: 'Cosmic timetraveler',
              src: 'https://tec.mx/sites/default/files/styles/slide_titular_desktop/public/repositorio/Home/alumnos-tec-de-monterrey.jpg?itok=7aJQrFe_',
              title: 'cosmic-timetraveler-pYyOZ8q7AII-unsplash.com',
          },
          {
              alt: 'Cristina Gottardi',
              src: 'https://tec.mx/sites/default/files/styles/slide_titular_desktop/public/repositorio/Home/tecscience-laboratorio-agro.jpg?itok=UfGiHpJS',
              title: 'cristina-gottardi-CSpjU6hYo_0-unsplash.com'
          },
          {
              alt: 'Johannes Plenio',
              src: 'https://tec.mx/sites/default/files/styles/slide_titular_desktop/public/repositorio/Home/filantropia-tec-de-monterrey-vinculacion.jpg?itok=gcvsZ-_D',
              title: 'johannes-plenio-RwHv7LgeC7s-unsplash.com'
          }
      ]
    </script>
<Carousel {images} duration={3000} imgClass="carousel" style="width:100%; height: 500px;"  let:Indicators >
    <Indicators />
</Carousel>
<img src="./images.png" style="margin-top:4px; width:100%;"/>