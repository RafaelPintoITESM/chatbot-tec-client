<!-- ChatWidget.svelte -->
<script lang="ts">
  
    let mostrarChat = false;
  
    function toggleChat() {
      mostrarChat = !mostrarChat;
    }

    let messages = [
        { mine:false , text: "Bienvenido, soy chatbot"},
    ]

    let sendMessage = ()=>{
        const entryMessage = { mine: true , text: newMessage};
        messages.push(entryMessage);
        messages = messages;
        newMessage = "";
    }

    let newMessage = "";
  </script>
  
  <style>
    .chat-button {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background-color: #0084ff;
      color: white;
      border: 3px solid;
      border-radius: 50%;
      width: 70px;
      height: 70px;
      font-size: 30px;
      cursor: pointer;
    }
  
    .chat-window {
  position: fixed;
  bottom: 100px;
  right: 20px;
  width: 500px;
  max-height: 400px;
  background-color: white;
  border: 1px solid #ccc;
  border-radius: 10px;
  overflow: hidden;
  display: flex;
  flex-direction: column;
}

/* Media query para pantallas de menos de 768px (dispositivos móviles) */
@media (max-width: 768px) {
  .chat-window {
    width: 95%; /* Ocupará el 95% del ancho de la ventana */
    right: 2.5%; /* Centra la ventana, dejando un margen igual a ambos lados */
    bottom: 100px; /* Ajusta la distancia desde la parte inferior en dispositivos móviles */
    max-height: 80vh; /* Opcional: ajusta la altura máxima para evitar que ocupe demasiado espacio vertical */
  }
}
  
    .chat-header {
      background-color: #0084ff;
      color: white;
      padding: 10px;
    }
  
    .chat-messages {
        display: flex;
        flex-direction: column;
        padding: 1rem;
    }
  
    .chat-input {
      display: flex;
      border-top: 1px solid #ccc;
    }
  
    .chat-input input {
      flex: 1;
      border: none;
      padding: 10px;
    }
  
    .chat-input button {
      background-color: #0084ff;
      color: white;
      border: none;
      padding: 0 20px;
      cursor: pointer;
    }

    .mensaje {
    max-width: 60%;
    padding: 0.5rem 1rem;
    border-radius: 8px;
    margin: 0.5rem 0;
    font-size: 0.9rem;
  }

  .mio {
    background-color: #d1e7dd;
    align-self: flex-end;
    text-align: right;
    color: #0f5132;
  }

  .otro {
    background-color: #d7e2f8;
    align-self: flex-start;
    text-align: left;
    color: #0252ff;
  }
  </style>
  
  {#if mostrarChat}
    <div class="chat-window">
      <div class="chat-header">
        <h3>Chat de Soporte</h3>
      </div>
      <div class="chat-messages">
        <!-- Aquí irían los mensajes del chat -->
        <p>Bienvenido al chat de soporte.</p>
        {#each messages as message}
            <div class="mensaje {message.mine ? 'mio' : 'otro'}">
                <p>{message.text}</p>
            </div>

        {/each}
      </div>
      <form on:submit|preventDefault={sendMessage}>
        <div class="chat-input">
                <input type="text" placeholder="Escribe un mensaje..."  bind:value={newMessage} />
                <button type="submit">Enviar</button>
        </div>
      </form>
    </div>
  {/if}
  
  <button class="chat-button" on:click={toggleChat}>
    💬
  </button>
  