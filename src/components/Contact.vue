<template>
  <div>
    <v-row>
      <v-col>
        <v-row
          class="mt-10 text-align-center animate-slide-fade-right"
        >
          <v-col>
            <v-container>
              <span
                class="text--secondary f40 mt-10"
              >
                CONTACT
              </span>
            </v-container>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-container>
          <v-form
            class="contact-form"
          >
            <v-row>
              <v-col>
                <v-text-field
                  label="Name"
                  :rules="name_rules"
                  hide-details="auto"
                  class="default-input"
                  outlined
                />  
              </v-col>
            </v-row>
            <v-row>
              <v-col>
                <v-text-field
                  label="E-mail"
                  :rules="email_rules"
                  hide-details="auto"
                  class="default-input"
                  outlined
                />  
              </v-col>
            </v-row>
            <v-row>
              <v-col>
                <v-text-field
                  label="Phone"
                  v-model="phone"
                  hide-details="auto"
                  class="default-input"
                  @keyup="formatPhone"
                />
              </v-col>
            </v-row>
            <v-row>
              <v-col>
                <v-textarea
                  label="Message"
                  v-model="message"
                  hide-details="auto"
                  class="default-input"
                />
              </v-col>
            </v-row>
            <v-row>
              <v-col>
                <v-btn
                  elevation="2"
                  class="submit-button py-5 d-flex align-center"
                >
                  SEND
                </v-btn>
              </v-col>
            </v-row>
          </v-form>
        </v-container>
      </v-col>
    </v-row>
    <v-divider class="my-10" />
    <v-row
      class="mx-10 mb-10 position-relative"
    >
      <v-col
        class="text-align-center"
      >
        <a 
          href="https://github.com/Felipe-A-Almeida"
          class="decoration-none f24"
        >
          <v-icon
            class="text--secondary"
          >
            mdi-github
          </v-icon>
          <span
            class="text--secondary"
          >
            GITHUB
          </span>
        </a>
      </v-col>
      <v-col
        class="text-align-center"
      >
        <a 
          href="https://www.linkedin.com/in/felipe-almeida-37b991159/"
          class="decoration-none f24"
        >
          <v-icon
            class="text--secondary"
          >
            mdi-linkedin
          </v-icon>
          <span
            class="text--secondary"
          >
            LINKEDIN
          </span>
        </a>
      </v-col>
      <v-col
        class="text-align-center"
      >
        <a 
          href="https://www.instagram.com/felipe.aug_/"
          class="decoration-none f24"
        >
          <v-icon
            class="text--secondary"
          >
            mdi-instagram
          </v-icon>
          <span
            class="text--secondary"
          >
            INSTAGRAM
          </span>
        </a>
      </v-col>
    </v-row>
  </div>
</template>

<script>

export default {
  data() {
    return {
      phone: '',
      email_regex: /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/,
      name_rules: [
        value => !!value || 'Required.',
        value => (value && value.length >= 3) || 'Min 3 characters',
        value => ((value.split(" ")).length > 1) || 'Insert your full name',
      ],
      email_rules: [
        value => !!value || 'Required',
        value => (this.email_regex.test(value))
      ],
      animation_list: [{
        caller: "animate-slide-fade-top",
        class: "slide-fade-top"
      }, {
        caller: "animate-slide-fade-right",
        class: "slide-fade-right"
      }],
    }
  },
  mounted() {
    const about_position = document.getElementById("contact").getBoundingClientRect();
    window.addEventListener("scroll", (event) => {
      let scroll = window.scrollY;
      if (scroll > about_position.top - 500) {
        this.animation_list.forEach(animation => {
          const divs = document.getElementsByClassName(animation.caller);
          Array.from(divs).forEach((div) => {
            div.classList.add(animation.class);
            div.classList.remove(animation.caller);
          })
        });
      }
    });
  },
  methods: {
    formatPhone(){
      if(this.phone.length > 15){
        this.phone = this.phone.slice(0,15);
        return false;
      };
      this.phone=this.phone.replace(/\D/g,"")
      this.phone=this.phone.replace(/^(\d\d)(\d)/g,"($1) $2")
      this.phone= (this.phone.length < 14) ?
        this.phone.replace(/(\d{4})(\d)/,"$1-$2") :
        this.phone.replace(/(\d{5})(\d)/,"$1-$2")
      return this.phone
    }
  }
}
</script>