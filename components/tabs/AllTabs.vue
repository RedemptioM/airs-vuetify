<template>
  <div>
    <v-tabs color="cyan" dark slider-color="yellow">
      <v-tab ripple>1 Select Subjects</v-tab>
      <v-tab ripple>2 Teaching Experience</v-tab>
      <v-tab ripple>3 Basic Information</v-tab>

      <v-tab-item>
        <v-card flat>
          <v-layout column>
            <v-flex xs12 md12>
              <p>Choose your subjects</p>
            </v-flex>
            <v-flex xs12 md12>
              <p>
                Select 1-5 subjects you'd like to tutor. You can add more later
                once you're done signing up.
              </p>
            </v-flex>
            <v-flex xs12 md4>
              <SubjectList />
            </v-flex>
            <v-flex xs12 md12>
              <div class="text-xs-center">
                <v-btn round color="primary" dark>Next</v-btn>
              </div>
            </v-flex>
          </v-layout>
        </v-card>
      </v-tab-item>

      <v-tab-item>
        <v-card flat>
          <v-layout column>
            <v-flex xs12 md12>
              <h1>Thanks {Alex}!</h1>
            </v-flex>
            <v-layout row>
              <v-flex xs6 align-self-center>
                <h2>Please tell us more about your teaching preferences.</h2>
              </v-flex>
              <v-flex xs6></v-flex>
            </v-layout>
            <v-flex xs12></v-flex>
            <v-flex xs12></v-flex>
            <v-layout row>
              <v-flex xs1></v-flex>
              <v-flex xs2 align-self-start>
                <h3>Have you ever been a teacher?</h3>
              </v-flex>
            </v-layout>
            <v-layout row>
              <v-flex xs1></v-flex>
              <v-flex xs6 align-self-start>
                <v-radio-group v-model="radios" :mandatory="false">
                  <v-radio label="Yes" value="Yes"></v-radio>
                  <v-radio label="No" value="No"></v-radio>
                </v-radio-group>
              </v-flex>
              <v-flex xs5></v-flex>
            </v-layout>
            <v-flex xs6></v-flex>
            <v-layout row>
              <v-flex xs1></v-flex>
              <v-flex xs2 align-self-start>
                <h3>Have many years of tutoring experience do you have?</h3>
              </v-flex>
            </v-layout>
            <v-layout row>
              <v-flex xs1></v-flex>
              <v-flex xs6 align-self-start>
                <v-radio-group v-model="radios" :mandatory="false">
                  <v-radio label="0" value="0"></v-radio>
                  <v-radio label="1" value="1"></v-radio>
                  <v-radio label="2-4" value="2"></v-radio>
                  <v-radio label="5-10" value="3"></v-radio>
                  <v-radio label="10+" value="4"></v-radio>
                </v-radio-group>
              </v-flex>
              <v-flex xs5></v-flex>
            </v-layout>
            <v-flex xs6></v-flex>
            <v-layout row>
              <v-flex xs1></v-flex>
              <v-flex xs2 align-self-start>
                <h3>Which type of students do you like to tutor?</h3>
              </v-flex>
            </v-layout>
            <v-layout row>
              <v-flex xs1></v-flex>
              <v-flex xs6 align-self-start>
                <v-radio-group v-model="radios" :mandatory="false">
                  <v-radio label="Elementary" value="Elementary"></v-radio>
                  <v-radio
                    label="Middle School"
                    value="Middle-School"
                  ></v-radio>
                  <v-radio label="High School" value="High-School"></v-radio>
                  <v-radio label="College" value="College"></v-radio>
                  <v-radio label="Adult" value="Adult"></v-radio>
                </v-radio-group>
              </v-flex>
              <v-flex xs5></v-flex>
            </v-layout>
            <v-flex xs12 md12>
              <div class="text-xs-center">
                <v-btn round color="primary" dark>Next</v-btn>
              </div>
            </v-flex>
          </v-layout>
        </v-card>
      </v-tab-item>

      <v-tab-item>
        <v-layout column>
          <v-flex xs12>
            <v-layout row>
              <v-flex xs6>
                <h1>Basic Information</h1>
              </v-flex>
              <v-flex xs6></v-flex>
            </v-layout>
          </v-flex>
          <v-flex xs12>
            <v-layout row>
              <v-flex xs6>
                <p>Please provide the basic information</p>
              </v-flex>
              <v-flex xs6></v-flex>
            </v-layout>
          </v-flex>
          <v-flex xs12></v-flex>
          <v-flex xs12></v-flex>
          <v-flex xs12>
            <v-layout row>
              <v-flex xs6>
                <v-layout column>
                  <v-flex xs6>
                    <h2>Administrative</h2>
                    <v-divider></v-divider>
                  </v-flex>
                  <v-flex xs6> </v-flex>
                  <v-flex xs6>
                    <p>Gender</p>
                    <v-overflow-btn></v-overflow-btn>
                  </v-flex>
                  <v-flex xs6></v-flex>
                  <v-flex xs6>
                    <p>Birthday</p>
                    <v-overflow-btn></v-overflow-btn>
                  </v-flex>
                  <v-flex xs6></v-flex>
                  <v-flex xs6>
                    <p>Cancellation notice</p>
                    <v-overflow-btn></v-overflow-btn>
                  </v-flex>
                  <v-flex xs6></v-flex>
                  <v-flex xs6>
                    <p>Where did you hear about Airstudy</p>
                    <v-overflow-btn></v-overflow-btn>
                  </v-flex>
                  <v-flex xs6></v-flex>
                  <v-flex xs6>
                    <h2>Hourly Rate</h2>
                  </v-flex>
                  <v-flex xs6></v-flex>
                  <v-flex xs6>
                    <p>Please choose an hourly rate to charge students.</p>
                  </v-flex>
                  <v-flex xs6></v-flex>
                  <v-flex xs6>
                    <v-text-field label="Hour Rate" solo></v-text-field>
                  </v-flex>
                  <v-flex xs6></v-flex>
                  <v-flex xs6></v-flex>
                  <v-flex xs6></v-flex>
                  <v-flex xs6>
                    <h1>Your addess</h1>
                    <v-divider></v-divider>
                  </v-flex>
                  <v-flex xs6> </v-flex>
                  <v-flex xs6>
                    <v-text-field
                      outline
                      clearable
                      label="Address"
                      type="text"
                    ></v-text-field>
                  </v-flex>
                  <v-flex xs6></v-flex>
                  <v-flex xs6>
                    <v-text-field
                      outline
                      clearable
                      label="Address 2"
                      type="text"
                    ></v-text-field>
                    <v-flex></v-flex>
                    <v-flex xs6>
                      <v-text-field
                        outline
                        clearable
                        label="City"
                        type="text"
                      ></v-text-field>
                    </v-flex>
                    <v-flex xs6>
                      <v-text-field
                        outline
                        clearable
                        label="State"
                        type="text"
                      ></v-text-field>
                    </v-flex>
                    <v-flex xs6>
                      <v-text-field
                        outline
                        clearable
                        label="Mailing ZIP code"
                        type="text"
                      ></v-text-field>
                    </v-flex>
                    <v-flex xs6>
                      <v-text-field
                        outline
                        clearable
                        label="Phone number"
                        type="text"
                      ></v-text-field>
                    </v-flex>
                  </v-flex>
                </v-layout>
              </v-flex>
              <v-flex xs1></v-flex>
              <v-flex xs4>
                <v-layout column>
                  <v-flex xs4>
                    <h2>Education</h2>
                    <v-divider></v-divider>
                  </v-flex>
                  <v-flex xs4></v-flex>
                  <v-text-field
                    outline
                    clearable
                    label="Undergraduate college"
                    type="text"
                  ></v-text-field>
                  <v-flex xs4></v-flex>
                  <v-flex xs4>
                    <v-text-field
                      outline
                      clearable
                      label="Undergraduate major"
                      type="text"
                    ></v-text-field>
                  </v-flex>
                  <v-flex xs4></v-flex>
                  <v-flex xs4>
                    <v-text-field
                      outline
                      clearable
                      label="Graduate college 1"
                      type="text"
                    ></v-text-field>
                  </v-flex>
                  <v-flex xs4></v-flex>
                  <v-flex xs4>
                    <v-text-field
                      outline
                      clearable
                      label="Type of degree"
                      type="text"
                    ></v-text-field>
                  </v-flex>
                  <v-flex xs4></v-flex>
                  <v-flex xs4>
                    <v-text-field
                      outline
                      clearable
                      label="Graduate college 2"
                      type="text"
                    ></v-text-field>
                  </v-flex>
                  <v-flex xs4></v-flex>
                  <v-flex xs4>
                    <v-text-field
                      outline
                      clearable
                      label="Type of degree"
                      type="text"
                    ></v-text-field>
                  </v-flex>
                  <v-flex xs4></v-flex>
                  <v-flex xs4>
                    <v-text-field
                      outline
                      clearable
                      label="Teaching certification"
                      type="text"
                    ></v-text-field>
                  </v-flex>
                </v-layout>
              </v-flex>
              <v-flex xs1></v-flex>
            </v-layout>
            <v-flex xs12 md12>
              <div class="text-xs-center">
                <v-btn round color="primary" dark>Next</v-btn>
              </div>
            </v-flex>
          </v-flex>
        </v-layout>
      </v-tab-item>
    </v-tabs>
  </div>
</template>

<script>
// import SubjectSelection from './tab1/SubjectSelection'
import SubjectList from './tab1/SubjectList'
export default {
  components: {
    SubjectList
  },
  data() {
    return {
      radios: 'Yes'
    }
  }
}
</script>

<style scoped></style>
