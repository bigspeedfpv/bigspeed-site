<script>
  import { onMount } from "svelte";

  import { fade } from "svelte/transition"

  let ready = false
  onMount(() => ready = true)
</script>

<svelte:head>
  <title>404 Not Found | bigspeed</title>
  <meta name="robots" content="noindex" />
</svelte:head>
{#if ready}
  <div in:fade={{delay: 500, duration: 1000}} class="container">
    <span class="gradient" />
  </div>
{/if}
<div class="container">
  <a sveltekit:prefetch href="/" class="status"><strong>404</strong></a>
</div>

<style>
  :global(html) {
    background-color: black;
  }

  .container {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;

    display: flex;
    justify-content: center;
    align-items: center;
  }

  .status {
    font-size: 120px;
    font-family: inherit;
    
    text-decoration: none;

    color: white;

    text-shadow: 0px 10px 20px rgba(0, 0, 0, 0.3);

    opacity: 50%;
  }

  .gradient {
    width: 350px;
    height: 125px;

    background: conic-gradient(from 180deg at 50% 50%, #FFB629 -135deg, #FF0099 50.63deg, #FFB629 225deg, #FF0099 410.62deg);
    opacity: 1;
    filter: blur(75px);
  }
</style>