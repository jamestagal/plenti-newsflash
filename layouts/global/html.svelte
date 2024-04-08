<script>
  import Footer from "./footer.svelte";
  import Head from "./head.svelte";
  import Header from "./header.svelte";
  import Login from "./login.svelte";
  import { onMount } from "svelte";

  export let content, layout, env, allContent, allLayouts, user;
  let hash;
  onMount(async () => {
    hash = window.location.hash;
  });
</script>

<html lang="en">
  <Head title={content.filename} {env} />
  <body>
    {#if user && $user.isAuthenticated}
      <svelte:component this={$user.menu} {user} bind:content={content} />
    {/if}
    <Login bind:hash {user} />
    <main>
      <Header {content}/>
      <svelte:component
        this={layout}
        {...content.fields}
        {allContent}
        {allLayouts}
        {content}
        {user}
      />
      <Footer />
    </main>
  </body>
</html>
