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
          width: 150px;
          display: inline-block;
          text-align: center;
          border: 1px solid lightgray;
          border-radius: 5px;
          margin: 5px;
          padding: 5px;
     }
     h1 {
          color: orangered;
          font-size: 140%;
     }
</style>
