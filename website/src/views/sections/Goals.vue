<template>
  <base-section id="goals">
    <base-section-heading title="Our Mission">
      Fork in the Road's mission is to support local restaurants during the COVID-19 pandemic through community donations.
    </base-section-heading>

    <v-container>
      <v-row>
        <v-col
          v-for="(feature, i) in features"
          :key="i"
          cols="12"
          md="6"
        >
          <base-avatar-card
            v-bind="feature"
            align="left"
            horizontal
          >
            {{feature.subtitle}}
          </base-avatar-card>
        </v-col>
      </v-row>
    </v-container>
  </base-section>
</template>

<script>
  export default {
    name: 'SectionGoals',

    data: () => ({
      features: [
        {
          color: 'primary',
          dark: true,
          title: 'Provide Necessary Equipment',
          subtitle: 'Donating portable tables and chairs for local restaurants to use for outdoor dining.',
          icon: 'mdi-fountain-pen-tip',
        },
        {
          color: 'primary',
          dark: true,
          title: 'Outreach',
          subtitle: 'Reaching out to other restaurants in the area. Collecting donations through GoFundMe. Visit the Donate page to contribute!',
          icon: 'mdi-cellphone',
        },
      ],
    }),
  }
</script>
