<script lang="ts">
  import { Button, CodeSnippet } from "carbon-components-svelte";
  import Camera16 from "carbon-icons-svelte/lib/Camera16";

  export let href: string;
</script>

<style lang="scss">
  .caption {
    position: absolute;
    bottom: 0;
    right: 0;
    max-width: 100%;
    display: inline-flex;

    :global(a) {
      cursor: pointer !important;
    }
  }
</style>

<div class="caption">
  <Button
    hasIconOnly
    icon={Camera16}
    iconDescription="Image source"
    tooltipPosition="right"
    tooltipAlignment="center"
    size="field"
    {href} />
  <CodeSnippet hideCopyButton>
    <slot />
  </CodeSnippet>
</div>
