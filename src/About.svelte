<script>
  import { Column, Grid, Link, Row } from "carbon-components-svelte";
  import DocumentPdf16 from "carbon-icons-svelte/lib/DocumentPdf16";
</script>

<style>
  h2 {
    margin: 1em 0;
  }
  p {
    margin-bottom: 1em;
  }
</style>

<section>
  <Grid>
    <Row>
      <Column>
        <h2>About me</h2>
        <p>
          Graduate software engineer, Computer Science, University of Lincoln,
          UK.
          <Link href="/static/Project.pdf" target="_blank">
            University Project
            <DocumentPdf16 />
          </Link>&#8288;.
        </p>
        <p>
          Experience with a variety of languages ranging from high to
          lower-level programming; including Go, C/C++, Rust, C#, JavaScript/TypeScript
          (NodeJS), and Haskell. Involvement and experience in teamwork
          utilising the agile development process and Git.
        </p>
        <p>
          Exposure to development tooling involving graphics frameworks such as
          OpenGL.
        </p>
        <p>
          A focus on creating desktop apps and tools, with particular interest
          in working with and contribution to open source projects and tools,
          including Linux.
        </p>
      </Column>
    </Row>
  </Grid>
</section>
