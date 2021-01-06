<script lang="ts">
  import {
    Column,
    Grid,
    Link,
    Row,
    StructuredList,
    StructuredListBody,
    StructuredListCell,
    StructuredListRow,
  } from "carbon-components-svelte";

  import type { Image } from "./common/types";

  interface Project {
    description: string;
    href: string;
    image: Image;
  }

  const projects: Project[] = [
    {
      description:
        "Pixsrt is a pixel sorter to glitch images, created in C++ with Qt.",
      href: "https://github.com/thorpelawrence/pixsrt",
      image: {
        src: "https://git.io/v77rh",
        alt: "Pixsrt",
      },
    },
    {
      description:
        "Spectrum Editor is a text editor with a ZX Spectrum theme, created with Electron and NodeJS.",
      href: "https://github.com/thorpelawrence/spectrum-editor",
      image: {
        src: "https://git.io/v77r7",
        alt: "Spectrum Editor",
      },
    },
    {
      description:
        "Connect Control for Spotify allows you to control Spotify Connect devices with Amazon Alexa.",
      href: "https://github.com/thorpelawrence/alexa-spotify-connect",
      image: {
        src: "https://git.io/vd4Iu",
        alt: "Connect Control for Spotify",
      },
    },
    {
      description:
        "Spectrum Editor is a text editor with a ZX Spectrum theme, created with Electron and NodeJS.",
      href:
        "https://play.google.com/store/apps/details?id=com.ReGroove.Wavehop",
      image: {
        src: "https://i.imgur.com/ANtDU8V.png",
        alt: "Spectrum Editor",
      },
    },
    {
      description:
        "Spectrum Editor is a text editor with a ZX Spectrum theme, created with Electron and NodeJS.",
      href: "https://github.com/thorpelawrence/quizics/blob/master/README.md",
      image: {
        src: "https://git.io/JfaVr",
        alt: "Spectrum Editor",
      },
    },
  ];
</script>

<style>
  img {
    max-width: 100px;
  }

  h2 {
    margin-top: 1em;
    margin-bottom: 0.5em;
  }

  section :global(.description) {
    vertical-align: middle;
  }
</style>

<section>
  <Grid>
    <Row>
      <Column>
        <h2>Projects</h2>
      </Column>
    </Row>
    <Row noGutter>
      <Column>
        <StructuredList>
          <StructuredListBody>
            {#each projects as { description, href, image: { src, alt } }}
              <StructuredListRow>
                <StructuredListCell>
                  <Link {href} target="_blank"><img {src} {alt} /></Link>
                </StructuredListCell>
                <StructuredListCell class="description">
                  <span>{description}</span>
                </StructuredListCell>
              </StructuredListRow>
            {/each}
          </StructuredListBody>
        </StructuredList>
      </Column>
    </Row>
  </Grid>
</section>
