<script lang="ts">
     let menu = true

     function toggle() {
          menu = !menu
     }
</script>

<ul>
     {#if menu}
          <li style="background-color: black;position: absolute;width: 100px;height: 100px;display: flex;justify-content: center;align-items: center;border-radius: 0 0 150% 0;">
               <button style="border: none;background-color: transparent; padding: 10px;position: absolute;top: 20px;left: 20px;" on:click={toggle}>
                    <svg width="35" height="5" style="background-color: white;border-radius: 5px;"/>
               </button>
          </li>
     {:else}
          <li style="background-color: black;position: absolute;width: 300px;height: 100vh;">
               <button style="border: none;background-color: transparent;padding: 10px;position: absolute;top: 20px; left: 20px;" on:click={toggle}>
                    <svg width="35" height="5" style="background-color: white;border-radius: 5px;"/>
               </button>
          </li>
          <ul style="position: absolute;left: 100px;top: 30%;color: white;font-size: 1.5rem;">
               <li>Some</li>
               <li>Some</li>
               <li>Some</li>
          </ul>
     {/if}
</ul>

