<script>
  import * as helpers from "@prismicio/helpers";

  export let contentLeft;
</script>

<div>
  <p>{@html helpers.asHTML(contentLeft)}</p>
</div>

<style>
  div {
    display: flex;
    flex-direction: column;
    margin-bottom: 1rem;
    text-align: left;
  }
</style>
