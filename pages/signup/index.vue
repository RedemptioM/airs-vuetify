<template>
  <v-container grid-list-md text-xs-center>
    <v-layout row wrap>
      <v-flex xs12 md12>
        <v-card color="white">
          <v-layout row>
            <v-flex xs12 md6>
              <h1>Tutor Sign Up</h1>
            </v-flex>
            <v-flex xs12 md6>
              <v-layout column>
                <v-flex xs12 md6>
                  <h2>Welcome, {Alex}!</h2>
                </v-flex>
                <v-flex xs12 md6>
                  <h2>Your username is {Alex}</h2>
                </v-flex>
              </v-layout>
            </v-flex>
          </v-layout>
        </v-card>
      </v-flex>

      <v-flex xs12 md12>
        <v-card color="white">
          <v-layout column>
            <v-flex xs12 md12>
              <h3>Subject Selection | 4 of 6 steps completed</h3>
            </v-flex>
            <v-flex xs12 md12>
              <ProcessBar />
            </v-flex>
            <v-flex xs12 md12>
              <AllTabs />
            </v-flex>
          </v-layout>
        </v-card>
      </v-flex>

      <v-flex xs12></v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import ProcessBar from '../../components/ProcessBar'
import AllTabs from '../../components/tabs/AllTabs'
export default {
  components: {
    ProcessBar,
    AllTabs
  }
}
</script>

<style scoped></style>
