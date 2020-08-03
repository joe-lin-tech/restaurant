<template>
  <base-section
    id="about-initiative"
  >
    <base-section-heading
      color="grey lighten-2"
      icon="mdi-vuetify"
      title="About the Initiative"
    />

    <v-container>
      <v-row>
        <v-col
          v-for="card in cards"
          :key="card.title"
          cols="12"
          md="4"
        >
          <base-info-card v-bind="card" />
        </v-col>
      </v-row>
    </v-container>
  </base-section>
</template>

<script>
  export default {
    name: 'SectionAboutInitiative',

    data: () => ({
      cards: [
        {
          title: 'Community Donations',
          subtitle: 'We need your help!',
          text: 'Collecting donations from the community to fund restaurant donations.',
          callout: '01',
        },
        {
          title: 'Purchase Equipment',
          subtitle: 'Equipment for restaurants',
          text: 'We purchase high quality restaurant equipment, such as tables and chairs to enable restaurants to start outdoor dining.',
          callout: '02',
        },
        {
          title: 'Restaurants',
          subtitle: 'Donations go directly to restaurants!',
          text: 'Restaurants will receive the equipment and start outdoor dining!',
          callout: '03',
        },
      ],
    }),
  }
</script>
