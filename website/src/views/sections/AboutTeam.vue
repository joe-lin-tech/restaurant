<template>
  <base-section
    id="about-team"
    class="pt-0"
  >
    <base-section-heading
      color="grey lighten-2"
      icon="mdi-vuetify"
      title="About the Team"
    />

    <v-container>
      <v-row>
        <v-col
          v-for="card in cards"
          :key="card.title"
          cols="12"
          md="12"
        >
          <base-profile-card v-bind="card" />
        </v-col>
      </v-row>
    </v-container>
  </base-section>
</template>

<script>
  export default {
    name: 'SectionAboutTeam',

    data: () => ({
      cards: [
        {
          title: 'Benjamin Fong',
          subtitle: 'CEO & Founder of Fork in the Road',
          text: 'Collecting donations from the community to fund restaurant donations.',
          callout: '01',
        },
      ],
    }),
  }
</script>
