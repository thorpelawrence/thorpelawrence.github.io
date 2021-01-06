<script>
  import {
    CodeSnippet,
    Content,
    Tile,
  } from "carbon-components-svelte";
  import copy from "clipboard-copy";
  import Caption from "./common/Caption.svelte";

  const username = "thorpe_lawrence";
</script>

<style lang="scss">
  :global(#main-content) {
    background-image: url("/images/enigma.jpg");
    background-size: cover;
    background-position: center;
    height: calc(100vh - 3rem);
  }

  .name :global {
    position: absolute;
    top: calc(30%);
    left: 50%;
    transform: translateX(-50%);
  }
</style>

<Content>
  <div class="name">
    <Tile light>
      <h1>Lawrence Thorpe</h1>
    </Tile>
    <CodeSnippet on:click={() => copy(username)}>{username}</CodeSnippet>
  </div>
  <Caption href="https://www.instagram.com/p/B78zyHhpHid/">
    Enigma Machine, Bletchley Park, Kodak TRI-X 400 +2, Lawrence Thorpe 2020
  </Caption>
</Content>
