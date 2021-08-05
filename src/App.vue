<template>
  <div id="app">
    <head>
      <meta charset="UTF-8">
      <meta http-equiv="X-UA-Compatible" content="IE=edge">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Caena</title>
      <!-- <link rel="stylesheet" href="css/style.css"> -->
    </head>
    <body>
    <div class="container">
        <nav class="navbar">
            <img src="@/assets/logo.svg" alt="caena logo" class="logo">
            <ul class="bar" id="nav">
                <li>
                  <a href="#"><img src="@/assets/dashboard.svg" alt="dash icon">Dashboard</a>
                </li>
                <li>
                  <a href="#"><img src="@/assets/questionnaire.svg" alt="question icon">Questionnaire<img src="@/assets/rightarrow.svg" alt="right arrow" class="rightarrow"></a>
                </li>
                <li>
                    <a href="#"><img src="@/assets/modeling.svg" alt="modeling icon">Financial Models</a>
                </li>
                <li>
                    <a href="#"><img src="@/assets/subscription.svg" alt="subscription icon">Subscriptions</a>
                </li>
                <li>
                    <a href="#"><img src="@/assets/paymenthist.svg" alt="payment icon">Payment History</a>
                </li>
                <li class="usericon">
                    <a href="#"><img src="@/assets/user.svg" alt="user icon">Johnathan Doe<img src="@/assets/downarrow.svg" alt="down arrow" class="downarrow"></a>
                </li>
            </ul>
        </nav>
        <div class="maincontainer">
            <h1>Questionnaire</h1>
            <form id="signup-form" @submit.prevent="submitForm">
              <div class="companyinfo">
                  <section class="sectionhead">
                    <img src="@/assets/sectionicon.svg" alt="section graphic" class="sectionlogo">
                    <div class="sectionheadtext">
                      <h3 class="header">Company Information</h3>
                      <p class="companydescript">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore</p>
                    </div>
                  </section>
                  <div class="questions">
                      <div class="list">
                          <ol>
                              <li>
                                <p>Company Name</p>
                                <input id="comp_name" type="text" placeholder="Company name" v-model="form.company">
                              </li>
                              <li>
                                <p>Company Email</p>
                                <input id="email" type="text" placeholder="e.g name@mail.com" v-model="form.email">
                              </li>
                              <li>
                                <p>Contact Number</p>
                                <input id="number" type="text" placeholder="Phone number" v-model="form.number">
                              </li>
                              <li>
                                <p>Country</p>
                                <select name="country" id="country" v-model="form.country">
                                    <option value="argentina">Argentina</option>
                                    <option value="australia">Australia</option>
                                    <option value="bahrain">Bahrain</option>
                                    <option value="belgium">Belgium</option>
                                    <option value="bosnia">Bosnia and Herzegovina</option>
                                    <option value="burkina">Burkina Faso</option>
                                    <option value="cote">Côte d'Ivoire</option>
                                    <option value="africa">Central African Republic</option>
                                    <option value="croatia">Croatia</option>
                                    <option value="denmark">Denmark</option>
                                    <option value="ethiopia">Ethiopia</option>
                                    <option value="germany">Germany</option>
                                </select>
                              </li>
                              <li>
                                  <p>State</p>
                                  <input type="text" placeholder="State" v-model="form.state">
                              </li>
                              <li>
                                  <p>City</p>
                                  <input type="text" placeholder="City" v-model="form.city">
                              </li>
                              <li>
                                  <p>Industry</p>
                                  <input type="text" placeholder="Select industry type" v-model="form.industry">
                              </li>
                              <li>
                                  <p>Company Website</p>
                                  <input type="text" placeholder="e.g www.company.com" v-model="form.website">
                              </li>
                              <li>
                                  <p>Company Description</p>
                                  <input type="text" placeholder="Description" v-model="form.description">
                              </li>
                              <li>
                                  <p>Company Stage</p>
                                  <input type="text" placeholder="Select stage" v-model="form.stage">
                              </li>
                              <li>
                                  <p>How many founders are involved in your startup?</p>
                                  <input type="text" placeholder="Founder size" v-model="form.size">
                              </li>
                          </ol>
                      </div>
                      <div class="termdef">
                          <div class="companyname">
                            <div class="term">
                                <h4>COMPANY NAME</h4>
                                <p>more explanation about "company name" to make user understand what it means</p>
                            </div>
                          </div>
                          <div class="industry">
                            <div class="term">
                                <h4>INDUSTRY</h4>
                                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor</p>
                            </div>
                          </div>
                          <div class="founders">
                            <div class="term">
                                <h4>FOUNDERS</h4>
                                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor</p>
                            </div>
                          </div>
                      </div>
                  </div>
              </div>
              <div class="founderinfo">
                  <section class="sectionhead">
                      <img src="@/assets/sectionicon.svg" alt="section graphic" class="sectionlogo">
                      <div class="sectionheadtext">
                          <h3 class="header">Founder Information</h3>
                          <p class="companydescript">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore</p>
                      </div>
                  </section>
                  <div class="questions">
                      <ol>
                          <li>
                              <p>Founder Full Name</p>
                              <input type="text" placeholder="Founder's name" v-model="form.founder">
                          </li>
                          <li>
                              <p>Founder Job Title</p>
                              <input type="text" placeholder="e.g CEO" v-model="form.job">
                          </li>
                          <li>
                              <p>Founder Email</p>
                              <input type="text" placeholder="e.g name@mail.com" v-model="form.founderemail">
                          </li>
                          <li>
                              <p>Founder LinkedIn URL</p>
                              <input type="text" placeholder="e.g linkedin.com/foundername" v-model="form.linkedin">
                          </li>
                      </ol>
                      <div class="termdef">
                          <div class="foundername">
                            <div class="term">
                                <h4>FOUNDER NAME</h4>
                                <p>we have sent an email to Johnathan@gmail with a link to verify your email. You need to verify your email to complete registration</p>
                            </div>
                          </div>
                      </div>
                  </div>
              </div>
              <div class="fundraise">
                  <section class="sectionhead">
                      <img src="@/assets/sectionicon.svg" alt="section graphic" class="sectionlogo">
                      <div class="sectionheadtext">
                        <h3 class="header">Fundraise & Traction</h3>
                        <p class="companydescript">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore</p>
                      </div>
                  </section>
                  <div class="questions">
                      <ol>
                          <li>
                            <p>Has your company previously raised any capital?</p>
                            <div class="mc">
                              <div class="form-check">
                                <input class="form-check-input" type="radio" name="capital" id="capital-yes" value="yes" v-model="form.capital">
                                <label class="form-check-label" for="capital">Yes</label>
                                <div class="check"></div>
                              </div>
                              <div class="form-check">
                                <input class="form-check-input" type="radio" name="capital" id="capital-no" value="no" v-model="form.capital">
                                <label class="form-check-label" for="capital">No</label>
                                <div class="check"></div>
                              </div>
                            </div>
                          </li>
                        <li>
                            <p>What is your estimated turnover for the current financial year?</p>
                            <input type="text" placeholder="Estimated turnover" v-model="form.turnover">
                        <li>
                            <p>Are you currently raising a funding round?</p>
                            <div class="mc">
                              <div class="form-check">
                                <input class="form-check-input" type="radio" name="fundinground" id="funding-yes" value="yes" v-model="form.fundinground">
                                <label class="form-check-label" for="fundinground">Yes</label>
                                <div class="check"></div>
                              </div>
                              <div class="form-check">
                                <input class="form-check-input" type="radio" name="fundinground" id="funding-no" value="no" v-model="form.fundinground">
                                <label class="form-check-label" for="fundinground">No</label>
                                <div class="check"></div>
                              </div>
                            </div>
                        </li>
                      </ol>
                      <div class="termdef">
                        <div class="companyname">
                            <div class="term">
                              <h4>CAPITALS</h4>
                              <p>we have sent an email to Johnathan@gmail with a link to verify your email. You need to verify your email to complete registration</p>
                            </div>
                        </div>
                      </div>
                  </div>
              </div>
              <a href="#" class="continue">Save & Continue</a>
            </form>
          </div>
      </div>
    </body>
  </div>
</template>

<script>
export default {
  name: 'Form',
  data () {
    return {
      form: {
        company: '',
        email: '',
        number: '',
        country: '',
        state: '',
        city: '',
        industry: '',
        website: '',
        description: '',
        stage: '',
        size: '',
        founder: '',
        job: '',
        founderemail: '',
        linkedin: '',
        capital: '',
        turnover: '',
        fundinground: ''
      }
    }
  },
  methods: {
    submitForm () {
      this.axios.post('/contact', this.form)
        .then((res) => {
          alert('success')
        })
        .catch((error) => {
          alert(error.response.status)
        }).finally(() => {
          alert('finally')
        })
    }
  }
}
</script>

<style>
#app {
  @import "./scss/main.scss";
  /* font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px; */
}
</style>
