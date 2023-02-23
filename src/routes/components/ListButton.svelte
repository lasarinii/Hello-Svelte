<script lang="ts">
     export let displayList: any
</script>

<button id="list" on:click={displayList}>
     <svg width="27" height="6" style="background-color: orangered;border-radius: 2px;display: block; margin:5px;"/>
     <svg width="27" height="6" style="background-color: orangered;border-radius: 2px;display: block; margin:5px;"/>
     <svg width="27" height="6" style="background-color: orangered;border-radius: 2px;display: block; margin:5px;"/>
</button>

<style>
     #list {
          transform: translateY(3px);
          border: none;
          border-radius:5px;
          background-color: lightgray;
     }
</style>
