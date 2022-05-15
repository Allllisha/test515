<script lang="ts">
  export let recipients : any

  console.log(recipients.join(",").length)
//   let sample = document.getElementsByClassName("svelte-1hjajnl");

// //はみ出したボックスの現在のCSS
// let style = window.getComputedStyle(sample);

// //フォントサイズとボックスの幅を数値で取得
// let fontsize = parseInt(style.fontSize);
// var width = parseInt(style.width);

// //２行分のボックスに収納できる文字数
// let mojisuu = Math.floor(width/fontsize)
// console.log(mojisuu);

</script>


{#if recipients.length === 1 }
<span>...</span>
{:else if recipients[0].length + recipients[1].length <= 37}
{`${recipients[0]}, ${recipients[1]}, ...`} 
{:else}
{`${recipients[0]}, ...`} 
{/if}