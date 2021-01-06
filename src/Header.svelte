<script>
  import {
    Header,
    HeaderActionLink,
    HeaderUtilities,
    SkipToContent,
  } from "carbon-components-svelte";
  import LogoGithub20 from "carbon-icons-svelte/lib/LogoGithub20";

  import ToggleTheme from "./ToggleTheme.svelte";
</script>

<Header platformName="lawrencethorpe.uk">
  <div slot="skip-to-content">
    <SkipToContent />
  </div>

  <HeaderUtilities>
    <HeaderActionLink
      href="https://github.com/thorpelawrence"
      target="_blank"
      icon={{ render: LogoGithub20 }} />
    <ToggleTheme />
  </HeaderUtilities>
</Header>
