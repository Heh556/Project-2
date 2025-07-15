<script>
import heroJson from './hero.json'
import monsterJson from './monsterDeck.json'
import itemJson from './itemDeck.json'
import * as math from 'mathjs';

// [import components here]
// remember to register them in the components property below!

export default {
  components: {
  },
  data() {
    return {
      hero: heroJson,
      itemDeck: itemJson,
      monsterDeck: monsterJson
    }
  },
  methods: {
    drawMonster() {
      let monsterCard = this.drawCard(this.monsterDeck)
      if (monsterCard) {
        let randomAction = math.randomInt(0, monsterCard.actions.length - 1)
        let action = monsterCard.actions[randomAction]
        this.hero[action.heroStatAffected] = math.evaluate(action.expression, this.hero)
        return monsterCard
      } else {
        return null
      }
    },
    drawItem() {
      let itemCard = this.drawCard(this.itemDeck)
      if (itemCard) {
        console.log("item", itemCard)
        this.hero[itemCard.heroStatAffected] = math.evaluate(itemCard.expression, this.hero)
        return itemCard
      } else {
        return null
      }
    },
    drawCard(deck) {
      if (deck.length !== 0) {
        const randomIndex = math.randomInt(0, deck.length - 1);
        const card = deck.splice(randomIndex, 1)[0];
        return card;
      } else {
        // deck is empty! HANDLE IT!
      }
    }
  },
  computed: {
  },
  mounted() {
  }
}
</script>

<template>
  <header>
    <h1>[Game Name Here]</h1>
  </header>

  <main>
    <!-- components here -->
  </main>

</template>

<style scoped></style>
