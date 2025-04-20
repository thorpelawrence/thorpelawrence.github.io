<script lang="ts">
  import { Link, Tooltip } from "carbon-components-svelte";
  import LogoGithub from "carbon-icons-svelte/lib/LogoGithub32";
  import LogoLinkedin from "carbon-icons-svelte/lib/LogoLinkedin32";
  import LogoInstagram from "carbon-icons-svelte/lib/LogoInstagram32";
  import LogoYoutube from "carbon-icons-svelte/lib/LogoYoutube32";
  import Email from "carbon-icons-svelte/lib/Email32";
  import BGG from "./icons/bgg.svg";
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
  <Link href="https://linkedin.com/in/thorpelawrence">
    <LogoLinkedin />
  </Link>
  <Link href="https://instagram.com/thorpe_lawrence">
    <LogoInstagram />
  </Link>
  <Link href="https://boardgamegeek.com/user/thorpe_lawrence" class="footer-icon">
    {@html BGG}
  </Link>
  <Link href="https://youtube.com/c/lawrencethorpe">
    <LogoYoutube />
  </Link>
  <Tooltip direction="top" icon={Email}>
    lawrence at lawrencethorpe dot uk
  </Tooltip>
</footer>
