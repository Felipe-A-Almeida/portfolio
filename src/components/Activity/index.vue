<template>
  <div>
    <v-row>
      <v-col
       cols="12"
      >
        <v-row
          class="mt-10 text-align-center animate-slide-fade-right"
        >
          <v-col>
            <v-container>
              <span
                class="text--secondary f40 mt-10"
              >
                ACTIVITIES
              </span>
            </v-container>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    <div
      class="activity-cards mb-0 pb-10 mx-5"
    >
      <ActivityCard
        v-for="(activity, index) in activites"
        :key="`activity_${index}`"
        class="animate-slide-fade-right"
        :title="activity.title"
        :description="activity.description"
        :icon="activity.icon"
      />
    </div>
  </div>
</template>

<script>
import ActivityCard from './ActivityCard.vue';
export default {
  components: {
    ActivityCard
  },
  data() {
    return {
      activites: [
        {
          title: 'Web Design',
          description: `
            Unlock the potential of your website design with our bespoke Figma templates 
            tailored to your unique brand identity and project requirements. Our service offers
            you the opportunity to streamline your design process while ensuring consistency, efficiency,
            and visual excellence by creating a responsive layout template using Figma.'
          `,
          icon: 'mdi-pencil-ruler'
        },
        {
          title: 'Landing Pages',
          description: `
            Empower your online presence with landing pages or portfolio websites
            tailored to showcase your unique story, skills, and offerings. This service combines creativity,
            strategy, and technical proficiency to deliver visually captivating and functionally effective digital
            experiences that leave a lasting impression and share your business.
          `,
          icon: 'mdi-application'
        },
        {
          title: 'Applications',
          description: `
            Empower your business to reach new heights with our custom systems solutions
            designed to streamline operations, increase efficiency and drive growth. Our service offers
            a strategic combination of technology expertise, industry insights and personalized support
            to deliver tangible results that make a real impact on your bottom line.
          `,
          icon: 'mdi-sitemap'
        }
      ]
    }
  }
}
</script>