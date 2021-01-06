<script lang="ts">
  import { HeaderGlobalAction } from "carbon-components-svelte";
  import Sun24 from "carbon-icons-svelte/lib/Sun24";
  import Moon24 from "carbon-icons-svelte/lib/Moon24";

  type Theme = "white" | "g10" | "g90" | "g100";
  const darkTheme: Theme = "g90";
  const lightTheme: Theme = "white";
  let theme: Theme = darkTheme;

  $: document.documentElement.setAttribute("theme", theme);
  $: darkMode = theme === darkTheme;

  function toggleDarkMode() {
    theme = darkMode ? lightTheme : darkTheme;
  }
</script>

<HeaderGlobalAction
  on:click={toggleDarkMode}
  icon={darkMode ? Sun24 : Moon24} />
