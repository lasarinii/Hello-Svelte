<script lang="ts">
     import List from './components/List.svelte'
     import ListButton from './components/ListButton.svelte';
     import Grid from './components/Grid.svelte'
     import GridButton from './components/GridButton.svelte';

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
     
{#if listgrid}
     <section style:padding="10px;">
          <GridButton displayGrid={displayGrid}/> 

          <ListButton displayList={displayList}/>
     
          <div id="show">
               {#if list}
                    <List nome={nome} items={show}/>
               {:else if grid}
                    <Grid nome={nome} items={show}/>
               {/if}
          </div>
     </section>
{/if}

<button on:click={toggle}>Click?</button>

<style> 
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
     button {
          margin: 50px;
          color: orangered;
          border: solid orangered 1px;
          border-radius: 5px;
          font-size: 1.3rem;
          padding: 5px;
          background-color: white;
     }
     #show {
          width: 500px;
          height: 500px;
          overflow-y: auto;
     }

</style>
