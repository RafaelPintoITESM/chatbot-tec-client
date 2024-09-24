<script lang="ts">
  import ChatWidget from './components/ChatWidget.svelte';
  import MyNavBar from './components/template/MyNavBar.svelte';
  import Home from './routes/Home.svelte';
  </script>
  
  <header>
    <MyNavBar />
  </header>
  <div class="mx-auto flex w-full">
    <main class="mx-auto lg:w-full">
      <div>
        <Home/>
        <ChatWidget/>
      </div>
    </main>
  </div>
  
  