<template>
  <div class="Welcome">
    <div class="application-container">
      <h1>Try the technology on desktop or mobile</h1>
      <v-btn class="app-btn margin-top-40" v-on:click="goToApplication()">
        <span>Launch application</span>
      </v-btn>
    </div>
    <div class="details">
      <div class="about">
        <h1>Machine learning to harness the power of your camera</h1>
        <div class="about-topics">
          <div class="topic">
            <h4 class="topic-heading">
              Computer vision
            </h4>
            <p>
              Our machine learning algorithm is trained with cutting edge
              technology, which has only become possible in recent years. With
              only the addition of software, cBMI can accurately estimate body
              mass index (BMI) from facial photos off of any camera.
            </p>
          </div>
          <div class="topic">
            <h4 class="topic-heading">
              Trained on a proprietary data set
            </h4>
            <p>
              Our team has built the largest known data set of labeled images
              for BMI. The accuracy we achieve is only possible with the raw
              scale of our verified, labeled images.
            </p>
          </div>
        </div>
        <div class="about-topics">
          <div class="topic">
            <h4 class="topic-heading">
              Elastic cloud compute, ready to scale
            </h4>
            <p>
              Built from day one with scalability in mind, we are ready to
              deploy our algorithm to millions. Using Google Cloud Platform
              services, we bring the reliability and security of big tech
              alongside our innovative work.
            </p>
          </div>
          <div class="topic">
            <h4 class="topic-heading">
              Only requires an internet connection
            </h4>
            <p>
              Designed to operate wherever people are working, exercising, or
              receiving care remotely, all we need is an internet connection
              capable of streaming video to our cloud.
            </p>
          </div>
        </div>
        <v-btn class="app-btn"
          >Read our white paper to learn more about performance</v-btn
        >
      </div>
      <div>
        <h1>Applications</h1>
        <div class="about-topics">
          <div class="topic">
            <v-img src="@/assets/img/pexels-andrea-piacquadio-3762940 1.png" />
          </div>
          <div class="topic">
            <h4 class="topic-heading">
              Only requires an internet connection
            </h4>
            <p>
              Designed to operate wherever people are working, exercising, or
              receiving care remotely, all we need is an internet connection
              capable of streaming video to our cloud.
            </p>
          </div>
        </div>

        <div class="about-topics" style="background-color: #F5F5F5;">
          <div class="topic">
            <h4 class="topic-heading">
              Fitness, wellness and diet
            </h4>
            <p>
              For sustained weight management it is so critical to maintain
              accountabiilty at all times -- frequent check-ins can mean the
              difference between weight loss and stagnation. A solution
              available on every smartphone an laptop means no excuses for
              fogetting to weigh in, it’s as easy as a notification and can be
              done wherever the day takes you.
            </p>
          </div>
          <div class="topic">
            <v-img src="@/assets/img/pexels-pixabay-34495 1.png" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Welcome",
  methods: {
    goToApplication() {
      this.$router.push("application");
    },
  },
};
</script>
<style>
.application-container {
  color: white;
  height: 378px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

/* .details {
} */
.about {
  padding: 20px 0;
}

.about-topics {
  margin-top: 20px;
  align-items: center;
  display: flex;
}

.topic {
  width: 50%;
  padding: 30px;
  text-align: left;
}

.topic-heading {
  font-weight: 700;
}

h1 {
  text-align: left;
  padding: 0 30px;
}
</style>
