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

  interface Certification {
    title: string;
    href: string;
    image: Image;
  }

  const certifications: Certification[] = [
    {
      title: "MTA: Database Fundamentals 2018",
      href:
        "https://www.youracclaim.com/badges/404bcfec-4dc1-4103-b4f8-e2ad71f3e31d/linked_in_profile",
      image: {
        src: "/images/certifications/mta-database-fundamentals-2018.png",
        alt: "MTA: Database Fundamentals 2018 Badge",
      },
    },
    {
      title: "MTA: Networking Fundamentals 2018",
      href:
        "https://www.youracclaim.com/badges/c8fc24bb-e24b-464d-8f39-bec5c8d42b57/linked_in_profile",
      image: {
        src: "/images/certifications/mta-networking-fundamentals-2018.png",
        alt: "MTA: Networking Fundamentals 2018 Badge",
      },
    },
    {
      title: "MTA: Security Fundamentals 2019",
      href:
        "https://www.youracclaim.com/badges/58ab4c62-1f70-4075-9bba-d401884be37d/linked_in_profile",
      image: {
        src: "/images/certifications/mta-security-fundamentals-2019.png",
        alt: "MTA: Security Fundamentals 2019 Badge",
      },
    },
    {
      title: "MTA: Cloud Fundamentals 2019",
      href:
        "https://www.youracclaim.com/badges/2f36501e-c674-4634-b1a0-fc294072d38c/linked_in_profile",
      image: {
        src: "/images/certifications/mta-cloud-fundamentals-2019.png",
        alt: "MTA: Cloud Fundamentals 2019 Badge",
      },
    },
    {
      title: "Google Cloud Platform Fundamentals: Core Infrastructure",
      href:
        "https://www.coursera.org/account/accomplishments/verify/ZPA4GGTX3KLW",
      image: {
        src: "/images/certifications/google-cloud-platform.png",
        alt: "Google Cloud Platform Logo",
      },
    },
  ];
</script>

<style>
  img {
    max-width: 100px;
  }

  h2 {
    margin-bottom: 0.5em;
  }

  section :global(.title) {
    vertical-align: middle;
  }
</style>

<section>
  <Grid>
    <Row>
      <Column>
        <h2>Certification</h2>
      </Column>
    </Row>
    <Row noGutter>
      <Column>
        <StructuredList>
          <StructuredListBody>
            {#each certifications as { title, href, image: { src, alt } }}
              <StructuredListRow>
                <StructuredListCell>
                  <Link {href} target="_blank"><img {src} {alt} /></Link>
                </StructuredListCell>
                <StructuredListCell class="title">
                  <span>{title}</span>
                </StructuredListCell>
              </StructuredListRow>
            {/each}
          </StructuredListBody>
        </StructuredList>
      </Column>
    </Row>
  </Grid>
</section>
