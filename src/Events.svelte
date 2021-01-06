<script>
  import {
    Column,
    Grid,
    ListItem,
    Row,
    Tile,
    UnorderedList,
  } from "carbon-components-svelte";
  import Laptop16 from "carbon-icons-svelte/lib/Laptop16";
  import Hashtag16 from "carbon-icons-svelte/lib/Hashtag16";
  import GameConsole16 from "carbon-icons-svelte/lib/GameConsole16";
</script>

<style lang="scss">
  h2 {
    margin-bottom: 1em;
  }

  section {
    margin-bottom: 2em;

    :global {
      li {
        span,
        svg {
          vertical-align: middle;
        }

        svg {
          margin-right: 0.6em;
        }
      }
    }
  }
</style>

<section>
  <Grid>
    <Row>
      <Column>
        <h2>Events</h2>
      </Column>
    </Row>
    <Row>
      <Column>
        <UnorderedList>
          <ListItem>
            <Laptop16 /><span>LincolnHack 2016, 2018</span>
          </ListItem>
          <ListItem>
            <Hashtag16 /><span>Google HashCode 2017, 2019</span>
          </ListItem>
          <ListItem>
            <GameConsole16 /><span>Global Game Jam 2017, 2019</span>
          </ListItem>
        </UnorderedList>
      </Column>
    </Row>
  </Grid>
</section>
