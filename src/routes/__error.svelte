<script context="module">
  import ErrorScreen from "./errorScreen.svelte";
  import NotFound from "./notFound.svelte";

  export let message;
  export let status;

  export function load({ error, status }) {
    return {
      props: {
        message: error.message,
        status, // same as status: status
      },
    };
  }
</script>

{#if status == 404}
  <!-- Used '==' instead of '===' to match string/number status code (just to be sure) -->
  <NotFound />
{:else}
  <ErrorScreen {message} {status} />
{/if}
