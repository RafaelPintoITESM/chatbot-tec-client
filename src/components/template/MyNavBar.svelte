<script lang="ts">
    import {
        Navbar,
        NavBrand,
        NavLi,
        NavUl,
        Dropdown,
        DropdownItem,
        DropdownDivider
    } from 'flowbite-svelte';
    import { BarsOutline, ChevronDownOutline, SearchOutline } from 'flowbite-svelte-icons';
    
    let divClass = 'w-full ml-auto lg:block lg:w-auto order-1 lg:order-none';
    let ulClass =
        'flex flex-col py-3 my-4 lg:flex-row lg:my-0 text-sm font-medium gap-4 dark:lg:bg-transparent lg:bg-white lg:border-0'; 
        
    </script>
<Navbar fluid="{true}">      
    <button>
      <BarsOutline size="xl"></BarsOutline>
    </button>
    <NavBrand href="/" class="lg:ml-2">
      <span class="self-center whitespace-nowrap pl-4 text-xl font-semibold dark:text-white">
        <img src="./logo.png" />
      </span>
    </NavBrand>
    <NavUl>
      <NavLi href="#">EDUCACIÓN</NavLi>
      <NavLi href="#">INVESTIGACIÓN</NavLi>
      <NavLi href="#">VINCULACIÓN</NavLi>
      <NavLi href="#">CONOCENOS</NavLi>
      <NavLi class="cursor-pointer">
        MÁS<ChevronDownOutline class="ms-2 inline h-6 w-6 text-primary-800 dark:text-white"></ChevronDownOutline>
      </NavLi>
      <Dropdown class="z-20 w-44">
        <DropdownItem href="#">PROFESORES</DropdownItem>
        <DropdownItem href="#">EGRESADOS</DropdownItem>
        <DropdownItem href="#">NOTICIAS</DropdownItem>
        <DropdownDivider></DropdownDivider>
        <DropdownItem href="#">TEC STORE</DropdownItem>
        <DropdownItem href="#">VENUES</DropdownItem>
        <DropdownItem href="#">CENTRO DE PRENSA</DropdownItem>
      </Dropdown>
      <NavLi href="#"></NavLi>
    </NavUl>
    <NavUl {divClass} {ulClass}  nonactiveclass="md:!pl-3 md:!py-2 lg:!pl-0 text-gray-700 hover:bg-gray-100 lg:hover:bg-transparent lg:border-0 lg:hover:text-primary-700 dark:text-white lg:dark:hover:text-primary-700 dark:hover:bg-gray-700 dark:hover:text-white lg:dark:hover:bg-transparent" activeclass="md:!pl-3 md:!py-2 lg:!pl-0 lg:text-primary-700 text-white dark:text-white dark:lg:text-primary-500 bg-primary-700 lg:bg-transparent dark:bg-primary-600 lg:dark:bg-transparent cursor-default">
      <div class="ml-auto flex items-center">
        <NavLi class="lg:mb-0 lg:px-2" href="#">
          ES | EN
        </NavLi>
        <NavLi class="cursor-pointer">
          mitec<ChevronDownOutline class="ms-2 inline h-6 w-6 text-primary-800 dark:text-white"></ChevronDownOutline>
        </NavLi>
        <Dropdown class="z-20 w-44">
          <DropdownItem href="#">ALUMNOS</DropdownItem>
          <DropdownItem href="#">PADRES</DropdownItem>
          <DropdownItem href="#">EGRESADORES</DropdownItem>
          <DropdownDivider></DropdownDivider>
          <DropdownItem href="#">PROFESORES</DropdownItem>
          <DropdownItem href="#">MARKET TEC</DropdownItem>
          <DropdownItem href="#">CENTRO DE PRENSA</DropdownItem>
        </Dropdown>
        <SearchOutline class="ml-10" size="xl"></SearchOutline>
      </div>
    </NavUl>
  </Navbar>
  
  
  <style>
    header {
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
    }
  </style>