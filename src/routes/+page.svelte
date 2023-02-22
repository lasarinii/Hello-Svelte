<script lang="ts">
     let nome = ""

     let grid = true
     let list = true

     function displayGrid() {
          grid = true
          list = false
     }
     function displayList() {
          list = true
          grid = false
     }
     
     let listgrid = false
     function toggle() {
          listgrid = !listgrid
     }

     let show = [
          {name: "1", content: "Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur cupidatat."},
          {name: "2", content: "Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur cupidatat."},
          {name: "3", content: "Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur cupidatat."},
          {name: "4", content: "Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur cupidatat."},
          {name: "5", content: "Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur cupidatat."},
          {name: "6", content: "Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur cupidatat."},
          {name: "7", content: "Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur cupidatat."},
          {name: "8", content: "Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur cupidatat."},
          {name: "9", content: "Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur cupidatat."},
          {name: "10", content: "Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur cupidatat."},
          {name: "11", content: "Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur cupidatat."},
          {name: "12", content: "Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur cupidatat."},
          {name: "13", content: "Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur cupidatat."},
          {name: "14", content: "Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur cupidatat."},
          {name: "15", content: "Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur cupidatat."},
          {name: "16", content: "Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur cupidatat."}
     ]
</script>

<h1>Bem vindo, {nome}<b>_</b>!</h1>
<input type="text" bind:value={nome} placeholder="Your name here">
     
<button on:click={toggle} style="color: orangered; border: solid orangered 1px;border-radius: 5px;font-size: 1.3rem;padding: 5px;position: absolute;bottom: 100px;background-color: white;">Click?</button>

{#if listgrid}
     <section>
          <button id="grid" on:click={displayGrid}>
               <svg width="13" height="13" style="background-color: orangered;border-radius: 2px;margin: 5px 0 -1px 5px;"/>
               <svg width="13" height="13" style="background-color: orangered;border-radius: 2px;margin: 5px 5px -1px 0;"/><br>
               <svg width="13" height="13" style="background-color: orangered;border-radius: 2px;margin: 0 0 2px 0;"/>
               <svg width="13" height="13" style="background-color: orangered;border-radius: 2px;margin: 0 0 2px 0;"/>
          </button>

          <button id="list" on:click={displayList}>
               <svg width="27" height="6" style="background-color: orangered;border-radius: 2px;display: block; margin:5px;"/>
               <svg width="27" height="6" style="background-color: orangered;border-radius: 2px;display: block; margin:5px;"/>
               <svg width="27" height="6" style="background-color: orangered;border-radius: 2px;display: block; margin:5px;"/>
          </button>
     
          <div id="show">
               {#if grid}
                    {#each show as item}
                         <div style="width: 150px; display: inline-block;text-align: center;border: 1px solid lightgray; border-radius: 5px;margin: 5px;">
                              <h1>Item: {item.name}</h1>
                              <p>{nome} {item.content}</p>
                         </div>
                    {/each}
               {:else if list}
                    {#each show as item}
                         <div style="border: 1px solid lightgray;margin: 5px;border-radius: 5px;">
                              <h1>Item: {item.name}</h1>
                              <p>{nome} {item.content}</p>
                         </div>
                    {/each}
               {:else}
                    <p>none</p>
               {/if}
          </div>
     </section>
{/if}

<style>
     :global(*) {
          margin: 0;
          padding: 0;
          box-sizing: border-box;
          font-family: Arial, Helvetica, sans-serif;
     }
     :global(body) {
          width: 100vw;
          height: 100vh;
          display: flex;
          justify-content: center;
          align-items: center;
          flex-direction: column;
     }
     h1 {
          font-size: 3rem;
          padding: 20px;
          color: orangered;
     }
     b {
          animation: underline 1s ease infinite;
     }
     @keyframes underline {
          0% {color: orangered}
          50% {color: transparent;}
     }
     section {
          padding: 10px;
     }
     #grid {
          border: none;
          border-radius: 5px;
          background-color: lightgray;
     }
     #list {
          transform: translateY(3px);
          border: none;
          border-radius:5px;
          background-color: lightgray;
     }
     #show {
          width: 500px;
          height: 500px;
          overflow-y: auto;
     }
     #show h1{
          font-size: 120%;
     }
</style>
