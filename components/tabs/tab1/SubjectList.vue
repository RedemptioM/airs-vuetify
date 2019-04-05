<template>
  <div class="text-md-center">
    <v-expansion-panel>
      <v-expansion-panel-content>
        <template v-slot:header>
          <div>English</div>
        </template>
        <v-card>
          <v-list>
            <v-list-tile>
              <v-list-tile-action>
                <v-checkbox v-model="englishStandard"></v-checkbox>
              </v-list-tile-action>
              <v-list-tile-content @click="englishStandard = !englishStandard">
                <v-list-tile-title>English Standard</v-list-tile-title>
              </v-list-tile-content>
            </v-list-tile>

            <v-list-tile>
              <v-list-tile-action>
                <v-checkbox v-model="englishAdvanced"></v-checkbox>
              </v-list-tile-action>
              <v-list-tile-content @click="englishAdvanced = !englishAdvanced">
                <v-list-tile-title>English Advanced</v-list-tile-title>
              </v-list-tile-content>
            </v-list-tile>
          </v-list>
        </v-card>
      </v-expansion-panel-content>
    </v-expansion-panel>
  </div>
</template>

<script>
// import { mapState } from 'vuex'
export default {
  name: 'SubjectList',
  data() {
    return {
      englishStandard: false,
      englishAdvanced: false
    }
  },
  computed: {
    subjectList() {
      return this.$store.state.signup.subjects
    },
    selectedSubject() {
      return []
    }
  }
}
</script>

<style scoped></style>
