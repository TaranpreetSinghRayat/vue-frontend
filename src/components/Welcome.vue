<template>
  <div class="Welcome">
    <div class="application-container">
      <div class="home-intro">
        <h1>
          <div style="font-size: 50px; font-weight: 200; line-height: 50px;">
            Try the
          </div>
          <div style="font-size: 55px; font-weight: 200; line-height: 55px;">
            technology
          </div>
          <div style="font-size: 53px; line-height: 53px;">on desktop</div>
          <div style="font-size: 50px; line-height: 50px;">or mobile</div>
        </h1>
        <v-btn
          style="margin: 20px;"
          class="app-btn"
          v-on:click="goToApplication()"
        >
          <span>Launch application</span>
        </v-btn>
      </div>
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
        <div class="about-topics">
          <div class="topic">
            <v-img
              style="width: 571px; height: 663px"
              src="@/assets/img/ID1@2x.png"
            />
          </div>
          <div class="topic">
            <h4>Application</h4>
            <h1 class="topic-heading">
              Remote Care And health
            </h1>
            <p>
              In A New World Now Ready To Treat Patients Anu Monitor Health
              Remotely, Cbmi Can Bring An Element Of Physiology To The Remote
              Paradigm. With A Smartphone In The Pocket Of 80% Of American
              Adults, We Are Magnitudes More Efficient Than Putting A Smart
              Scale In Every Home.
            </p>
          </div>
        </div>

        <div class="about-topics" style="background-color: #F5F5F5;">
          <div class="topic">
            <h4>Application</h4>
            <h1 class="topic-heading">
              Fitness, wellness and diet
            </h1>
            <p>
              For Sustained Weight Management It Is So Critical To Maintain
              Accountability At All Times -- Frequent Check-Ins Can Mean The
              Difference Between Weight Loss And Stagnation. A Solution
              Available On Every Smartphone An Laptop Means No Excuses For
              Fogetting To Weigh In, It's As Easy As A Notification And Can Be
              Done Wherever The Day Takes You.
            </p>
          </div>
          <div class="topic">
            <v-img src="@/assets/img/pexels-pixabay-34495 1.png" />
          </div>
        </div>
      </div>
    </div>
    <div style="padding:60px">
      <h1>About cumulative intelligence</h1>
      <h4>
        Formed in the wake of the pandemic's remote revolution, we build for a
        purpose
      </h4>
      <div class="about-application">
        <v-img
          style="width: 200px; margin: 30px"
          src="@/assets/img/ID1567964970614@2x.png"
        />
        <div style="text-align: left;">
          <h3>
            Jacob Fure-Slocum
          </h3>
          <h6>
            President:
          </h6>
          <p>
            Jacob is an MBA candidate at MIT Sloar. who has worked in the
            computer vision space for the last two years in various roles. He is
            a graduate of the University of Chicago, was a Summer Associate with
            Bain & Company, and has led teams before as a Marine Officer.
          </p>
        </div>
      </div>
      <div class="about-application">
        <v-img
          style="width: 200px; margin: 30px"
          src="@/assets/img/ID1544331164404@2x.png"
        />
        <div style="text-align: left;">
          <h3>
            Sid Beaumaster
          </h3>
          <h6>
            Technical Director:
          </h6>
          <p>
            Sid has spent the last four years in data science roles at Harvard
            Business School, the University of Southern California, and the
            University of Wisconsin, where she majored in mathematics. She is a
            constant learner and full stack developer.
          </p>
        </div>
      </div>
    </div>
    <div class="know-about-us">
      <h1>Want To Learn More?</h1>
      <input placeholder="First Name " />
      <input placeholder="Last name " />
      <input placeholder="Email Address " />
      <input placeholder="Phone Number " />
      <textarea style=" height: 200px" placeholder="Tell us more" />

      <v-btn style="width: 80%">submit Response</v-btn>

      <div class="footer">
        <v-img
          style="width: 40px"
          src="@/assets/img/cumulative-logo-final-5B5D45_bjd.png"
        />
        <span style="font-size: 12px">Creative_Cumulative</span>
      </div>
    </div>
    <div
      style="border-top: 1px solid white; background-color: #525347; color: white; height: 40px"
    >
      <h5>Cumulative_intelligence Corp, 2021</h5>
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
  height: 502px;
  display: flex;
  justify-content: center;
  flex-direction: column;
}

/* .details {
} */
.about {
  padding: 20px 0;
  background: #f8f8f8;
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

.home-intro {
  width: 30%;
  text-transform: uppercase;
  text-align: left;
  margin: 0 4em;
}

.about-application {
  display: flex;
  justify-content: center;
  align-items: center;
}

input,
textarea {
  border: 2px solid white;
  width: 80%;
  padding: 0 20px;
  margin: 10px 0;
  color: white;
}

::placeholder {
  color: white;
}

.know-about-us {
  padding: 60px;
  background-color: #525347;
  color: white;
  justify-content: center;
  display: flex;
  align-items: center;
  flex-direction: column;
}

.footer {
  margin: 40px;
  display: flex;
  justify-content: center;
  align-items: center;
}

hr {
  width: 100%;
  border-top: 1px solid white;
}
</style>
