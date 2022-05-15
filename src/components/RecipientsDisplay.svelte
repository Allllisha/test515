<script lang="ts">
  export let recipients: any

  // console.log(recipients.join(',').length)
  
  let sample = document.getElementsByClassName('svelte-1hjajnl')

  let style = window.getComputedStyle(sample)

  let fontsize = parseInt(style.fontSize)
  var width = parseInt(style.width)

  let howMany = Math.floor(width / fontsize)
  console.log(howMany)
</script>

{#if recipients.length === 1}
  <span>...</span>
{:else if recipients[0].length + recipients[1].length <= 37}
  {`${recipients[0]}, ${recipients[1]}, ...`}
{:else}{`${recipients[0]}, ...`}{/if}
