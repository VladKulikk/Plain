<template>
  <header>
    <img alt="logo" src="./assets/logo.svg">
    <nav>
      <p>Missions</p>
      <p>Jobs <span class="jobs-amount-indicator">3</span></p>
      <button id="earlyAccess">Get early access <img alt="arrow" src="./assets/arrow.svg"></button>
    </nav>
  </header>
  <main>
    <section class="preview-section">
      <div class="preview-text">
        <p class="preview-header-text">The customer service platform<br><img alt="" src="./assets/enter-arrow.svg">
          designed to be build with.</p>
        <p id="greeting">Say hello to Plain - the customer service platform for modern companies. A beautiful,
          lightning-fast app, backed by the same powerful API you can use directly. Plain and simple.</p>
        <button class="request-eap">Request early access</button>
      </div>
      <div class="preview-img-container">
        <img alt="preview" class="preview-image" src="./assets/title.png">
      </div>
    </section>

    <section class="services-section">
      <ServiceComponent
          icon="assets/plug-and-play-icon.svg"
          text="Plain comes with everything you need to get going in minutes: An app for your advisors, issue management, chat, email, calls (soon) and powerful reporting."
          title="Plug & play"
      ></ServiceComponent>
      <ServiceComponent
          icon="assets/build-api-icon.svg"
          text="Integrate Plain as much or as little as you want – or even build on top of it. Our API is built to work with your own systems and gives you full programmatic control."
          title="Build API-first"
      ></ServiceComponent>
      <ServiceComponent
          icon="assets/respects-data.svg"
          text="Plain doesn’t store your customer data, you do. Rather than you syncing data with us, we'll fetch just-in-time from you and discard it when you tell us to."
          title="Respects your data"
      ></ServiceComponent>
    </section>

    <section id="list-section">
      <ServiceComponent1
          :items="[
              'Plain gives you a single timeline for each customer, no more duplicate tickets or multiple threads to track down',
              'The timeline contains all your customer interactions, so you always know who did what and when',
              'It can show custom events specific to your operation so you know the full customer journey',
          ]"
          img="assets/orders.png"
          listIndicator="circle-list-indicator"
          title="One time to contain everything and anything"
      ></ServiceComponent1>
      <ServiceComponent1
          :items="[
              'Issues track the problems customers are experiencing, without breaking conversations up into tickets',
              'They can be opened and resolved at any point and are all visible in the customer timeline',
              'Each issue is based on a type set by you, giving you accurate tracking and actionable metrics',
          ]"
          img="assets/issues.png"
          listIndicator="rhombus-list-indicator"
          title="All the rigour of tickets, none of the pain"
      ></ServiceComponent1>
      <ServiceComponent1
          :items="[
              'Show advisors rich, real-time information from your own systems and reduce tab switching',
              'Configure what you show via a simple API without syncing, iframes or apps',
              'Maintain complete control of your data with fully customisable caching policies and expiries',
          ]"
          img="assets/recent-orders.png"
          listIndicator="rhombus-list-indicator"
          title="Incredibly simple, infinitely adaptable"
      ></ServiceComponent1>
    </section>

    <section id="blackBackground">
      <img id="imgPoints" :src="require('@/assets/dotted-grid.svg')" alt="points">
      <div id="mission-title-div"><h1 id="mission-title">Why we are building <br>Plain API-first</h1></div>
      <div id="mission-text">
        <p class="engineering-text">Over the last decade, engineering infrastructure across virtually every company area
          has become more advanced: Payments, communications, data, and so forth. What used to take teams in high-growth
          companies entire quarters to accomplish now takes individual engineers a few days.</p>
        <p class="engineering-text">This shift has happened in every area but customer service. There, the choice
          remains between maintaining a patchwork of hacks, fighting the rigid structures of established platforms, or
          wiring together cloud call centre solutions and building homegrown ticketing systems.</p>
        <p class="engineering-text">We are building Plain to change this - to make great customer service, at every
          scale, plain and simple.</p>
        <button id="mission-reading">Read our mission <img alt="arrow" src="./assets/arrow.svg"></button>
      </div>
    </section>
    <section id="workUpdates">
      <RouteComponent
        icon="assets/work-with-us.svg"
        title="Work with us"
        text="We are hiring designers and engineers of all levels. Come help us build the customer service infrastructure for modern companies."
        >
        <button id="view">View 3 open roles</button>
      </RouteComponent>
      <RouteComponent
          icon="assets/sign-up-for-updates-icon.svg"
          title="Sign up for updates"
          text="Join us on our journey! We'll send you an update every couple of months on our progress and what we're up to."
      >
        <div id="e-mailArea">
          <input type="email" placeholder="Your e-mail" id="e-mail">
          <button id="sign">Sign up</button>
        </div>
      </RouteComponent>
    </section>

    <footer>
      <img alt="logo" src="./assets/logo.svg">
      <div>
        <a id="not-just-text">Not Just Tickets LTD.</a>
        <a>Privacy Policy</a>
        <a>Privacy Notice</a>
        <p>@builtwithplain</p>
      </div>
    </footer>
  </main>
</template>

<script>
import ServiceComponent from './components/Service.vue'
import ServiceComponent1 from './components/ItemInfo.vue'
import RouteComponent from './components/Roles.vue'

export default {
  name: 'App',
  components: {
    ServiceComponent,
    ServiceComponent1,
    RouteComponent
  }
}
</script>

<style>
#app {
  font-family: Roboto, sans-serif;
  overflow-x: hidden;
}

body{
  margin: 0;
  display: flex;
  flex-flow: column;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;

  padding: 0 150px;
}

header nav {
  display: flex;
  gap: 15px;

  align-items: center;
}

header nav p {
  display: flex;
}

.jobs-amount-indicator {
  display: grid;
  place-items: center;

  width: 20px;
  height: 20px;

  background-color: indianred;
  margin-left: 5px;
}

header nav button {
  display: flex;
  height: 25px;
  align-items: center;
  justify-content: space-between;
  width: 150px;

  border: solid 2px lightgray;
  border-radius: 2px;

  background: transparent;
}

main {
  margin-top: 75px;
}

.preview-section {
  display: flex;

  height: 750px;
}

.preview-text {
  display: flex;
  flex-flow: column;
}

.preview-header-text {
  font-family: 'Roboto', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 60px;
  line-height: 69px;
}

#greeting {
  font-weight: 400;
  font-size: 18px;
  line-height: 27px;

  color: rgba(0, 0, 0, 0.6);

  width: 50%;
}

.preview-img-container {
  position: relative;
}

.preview-image {
  position: absolute;
  left: -350px;
}

.request-eap {
  width: 200px;

  border-radius: 3px;

  background: black;

  color: white;

  font-weight: 400;
  font-size: 15px;
  line-height: 22px;
}

.services-section {
  display: flex;
  flex-flow: row;
  justify-content: space-between;
}

#list-section {
  margin: 40px 0;
}

#blackBackground {
  background: black;

  display: grid;
  grid-template-columns: 50% 50%;

  margin: 200px 0;

  height: 300px;

  padding: 170px 0;
}

#mission-title-div {
  grid-row: 1;
  grid-column: 1;

  display: flex;
  justify-content: center;
}

#mission-title {
  color: white;
}

#mission-text {
  display: flex;
  flex-flow: column;
  text-align: left;

  font-weight: 400;
  font-size: 18px;
  line-height: 27px;

  grid-row: 1;
  grid-column: 2;
}

.engineering-text {
  color: white;

  font-weight: 400;
  font-size: 18px;
  line-height: 27px;
}

#mission-reading {
  display: flex;
  height: 25px;
  align-items: center;
  justify-content: space-around;
  width: 30%;
}

#imgPoints {
  grid-row: 1;
  grid-column: 1;
}

#workUpdates{
  display: flex;
  flex-flow: row;
  justify-content: space-around;
}

#view{
  width: 50%;

  color: white;
  background: black;

  border-radius: 2px;

  margin-top: 30px;
}

#e-mailArea{
  margin-top: 30px;
  width: 70%;

}

#e-mail{
  width: 70%;

  border: lightgray solid 2px;
  border-radius: 2px;

  height: 30px;

  padding-left: 20px;
}

#sign{
  background: black;
  color: white;

  height: 34px;

  margin-left: 10px;

  border-radius: 2px;
}

footer{
  display: flex;

  justify-content: space-between;
  align-items: center;

  padding: 0 150px;

  margin-top: 150px;
}

footer div{
  display: flex;
  gap: 30px;

  align-items: center;
}

#not-just-text{
  color: rgba(0 0 0 / 0.6);
}

section{
  padding: 0 100px;
}
</style>
