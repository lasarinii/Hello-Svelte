<script lang="ts">
     export let items: any
     export let nome: any
</script>

{#each items as item}
     <div>
          <h1>Item: {item.name}</h1>
          <p>{nome} {item.content}</p>
     </div>
{/each}

<style>
     div {
          width: 480px;
          border: 1px solid lightgray;
          margin: 5px;
          border-radius: 5px;
          padding: 5px;
     }
     h1 {
          color: orangered;
          font-size: 140%;
     }
</style>
