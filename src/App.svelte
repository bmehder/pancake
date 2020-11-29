<script>
  // Data
  import { tabData } from "./Data/tabData.js";

  // Layout Components
  import Header from "./Layouts/Header.svelte";
  import Section from "./Layouts/Section.svelte";
  import Footer from "./Layouts/Footer.svelte";

  // UI Components
  import Button from "./UI/Button.svelte";
  import Hero from "./UI/Hero.svelte";
  import CTA from "./UI/CTA.svelte";
  import FancyCard from "./UI/FancyCard.svelte";
  import Tabs from "./UI/Tabs.svelte";
  import Form from "./UI/Form.svelte";

  // Content Components
  import HomeContent from "./Content/HomeContent.svelte";
</script>

<Header uppercase background="coral" width="150px" />

<Hero
  title="The Demo is Off and Running."
  backgroundImage="https://source.unsplash.com/random/1600x600/">
  <Button
    shadow
    rounded
    reflection
    uppercase
    background="linear-gradient(to bottom, rgba(0,0,0,0.75), dodgerblue)"
    color="rgba(255,255,255,0.8)">
    Make My Day
  </Button>
</Hero>

<Section>
  <HomeContent />
  <Tabs data={tabData} width="600px" />
  <Button reflection uppercase background="coral">I Dare You</Button>
</Section>

<Hero
  full
  background="coral"
  title="Hey, look. It's a full screen hero component.">
  <CTA
    heading="This is HUGE"
    subtitle="You don't want to miss out."
    buttonText="Break Glass" />
</Hero>

<Section full>
  <div class="two-col">
    <FancyCard
      raise
      center
      title="Item 1"
      content="Lorem ipsum dolor sit amet" />
    <FancyCard
      raise
      ribbon
      center
      title="Item 2"
      content="Lorem ipsum dolor sit amet" />
  </div>
  <FancyCard
    ribbon
    raise
    title="Item 3"
    content="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " />
</Section>

<Hero background="dodgerblue">
  <Form
    title="Send Us A Message"
    buttonColor="coral"
    buttonTextColor="white"
    buttonText="Send Message" />
</Hero>

<Section>
  <div class="two-col">
    <FancyCard />
    <FancyCard ribbon />
  </div>
</Section>

<Footer background="#394149" color="white">
  &copy; 2020 Brad Mehder. All rights reserved.
</Footer>
