<script lang="ts">
  import { Link } from "carbon-components-svelte";
  import LogoGithub from "carbon-icons-svelte/lib/LogoGithub32";
  import LogoLinkedin from "carbon-icons-svelte/lib/LogoLinkedin32";
  import LogoTwitter from "carbon-icons-svelte/lib/LogoTwitter32";
  import LogoInstagram from "carbon-icons-svelte/lib/LogoInstagram32";
  import LogoSnapchat from "carbon-icons-svelte/lib/LogoSnapchat32";
  import LogoFacebook from "carbon-icons-svelte/lib/LogoFacebook32";
  import LogoYoutube from "carbon-icons-svelte/lib/LogoYoutube32";
  import Email from "carbon-icons-svelte/lib/Email32";
</script>

<style lang="scss">
  footer {
    height: 4rem;
    padding: 1rem 10px;
    display: flex;
    justify-content: space-around;
  }
</style>

<footer>
  <Link href="https://github.com/thorpelawrence">
    <LogoGithub />
  </Link>
  <Link href="https://www.linkedin.com/in/thorpelawrence/">
    <LogoLinkedin />
  </Link>
  <Link href="https://twitter.com/thorpe_lawrence">
    <LogoTwitter />
  </Link>
  <Link href="https://instagram.com/thorpe_lawrence">
    <LogoInstagram />
  </Link>
  <Link href="https://www.snapchat.com/add/thorpe_lawrence">
    <LogoSnapchat />
  </Link>
  <Link href="https://www.facebook.com/thorpe.lawrence">
    <LogoFacebook />
  </Link>
  <Link href="https://www.youtube.com/c/lawrencethorpe">
    <LogoYoutube />
  </Link>
  <Link href="mailto:lawrence@lawrencethorpe.uk">
    <Email />
  </Link>
</footer>
