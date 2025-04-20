<script lang="ts">
  import links from "./links.json";
  import { Link, Tooltip } from "carbon-components-svelte";
  import LogoGithub from "carbon-icons-svelte/lib/LogoGithub32";
  import LogoLinkedin from "carbon-icons-svelte/lib/LogoLinkedin32";
  import LogoInstagram from "carbon-icons-svelte/lib/LogoInstagram32";
  import LogoYoutube from "carbon-icons-svelte/lib/LogoYoutube32";
  import Email from "carbon-icons-svelte/lib/Email32";
  import BGG from "./icons/bgg.svg";

  const shortLinks = Object.keys(links).reduce((acc, name) => {
    acc[name] = `/l/${name}`;
    return acc;
  }, {});
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
  <Link href={shortLinks.gh}>
    <LogoGithub />
  </Link>
  <Link href={shortLinks.in}>
    <LogoLinkedin />
  </Link>
  <Link href={shortLinks.ig}>
    <LogoInstagram />
  </Link>
  <Link href={shortLinks.bgg}>
    {@html BGG}
  </Link>
  <Link href={shortLinks.yt}>
    <LogoYoutube />
  </Link>
  <Tooltip direction="left" icon={Email}>
    lawrence at lawrencethorpe dot uk
  </Tooltip>
</footer>
