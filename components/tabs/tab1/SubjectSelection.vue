<template>
  <v-tab-item>
    <v-card flat>
      <v-layout column>
        <v-flex xs12 md12>
          <p>Choose your subjects</p>
        </v-flex>
        <v-flex xs12 md12>
          <p>
            Select 1-5 subjects you'd like to tutor. You can add more later once
            you're done signing up.
          </p>
        </v-flex>
        <v-flex xs12 md4>
          <SubjectList />
        </v-flex>
        <v-flex xs12 md12>
          <v-btn>
            <div class="text-xs-center">
              <v-btn round color="primary" dark>Next</v-btn>
            </div>
          </v-btn>
        </v-flex>
      </v-layout>
    </v-card>
  </v-tab-item>
</template>

<script>
import SubjectList from './SubjectList'
export default {
  name: 'SubjectSelection',
  components: {
    SubjectList
  }
}
</script>

<style scoped></style>
