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
        "Connect Control for Spotify allows you to control Spotify Connect devices with Amazon Alexa.",
      href: "https://github.com/thorpelawrence/alexa-spotify-connect",
      image: {
        src: "https://git.io/vd4Iu",
        alt: "Connect Control for Spotify",
      },
    },
    {
      description:
        "Wavehop is an endless runner game where each jump button changes your colour, created for GGJ2017.",
      href:
        "https://play.google.com/store/apps/details?id=com.ReGroove.Wavehop",
      image: {
        src: "https://i.imgur.com/ANtDU8V.png",
        alt: "Wavehop",
      },
    },
    {
      description: "npm-github-packages-auth-helper is a tool written in TypeScript to manage npm token storage using system keychain.",
      href: "https://github.com/thorpelawrence/npm-github-packages-auth-helper",
      image: {
        src:
          "https://github.com/thorpelawrence/npm-github-packages-auth-helper/raw/main/images/logo-keyring.png",
        alt: "npm-github-packages-auth-helper",
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
        "Quizics is a C# physics quiz for teachers/students, originally completed for Computing A-Levels.",
      href: "https://github.com/thorpelawrence/quizics/blob/master/README.md",
      image: {
        src: "https://git.io/JfaVr",
        alt: "Quizics",
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
