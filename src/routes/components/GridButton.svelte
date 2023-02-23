<script lang="ts">
     export let displayGrid: any
</script>

<button id="grid" on:click={displayGrid}>
     <svg width="13" height="13" style="background-color: orangered;border-radius: 2px;margin: 5px 0 -1px 5px;"/>
     <svg width="13" height="13" style="background-color: orangered;border-radius: 2px;margin: 5px 5px -1px 0;"/><br>
     <svg width="13" height="13" style="background-color: orangered;border-radius: 2px;margin: 0 0 2px 0;"/>
     <svg width="13" height="13" style="background-color: orangered;border-radius: 2px;margin: 0 0 2px 0;"/>
</button>

<style>
     #grid {
          border: none;
          border-radius: 5px;
          background-color: lightgray;
     }
</style>
