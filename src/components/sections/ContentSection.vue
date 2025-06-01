<template>
  <div class="content-section-wrapper">
    <TextBlock>
      <template #special-title>
        <h1>
          We make <a href="" class="title-link">Live</a>, <a href="" class="title-link">Push</a>,
          <a href="" class="title-link">Note</a>, <a href="" class="title-link">Move</a> and
          <a href="" class="title-link">Link</a> — unique software and hardware for music creation
          and performance. With these products, our community of users creates amazing things.
        </h1>
      </template>
      <template #text>
        <p>
          Ableton was founded in 1999 and released the first version of Live in 2001. Our products
          are used by a community of dedicated musicians, sound designers, and artists from across
          the world.
        </p>
      </template>
    </TextBlock>
    <ImageBlock
      images="https://ableton-production.imgix.net/about/photo-1.jpg?fit=crop"
      color="var(--color-content-bg-1)"
    >
      <template #color-block-content></template>
    </ImageBlock>
    <TextBlock
      title="Making music isn’t easy. It takes time, effort, and learning. But when you’re in the flow, it’s incredibly rewarding."
    >
      <template #text>
        <p>
          We feel the same way about making Ableton products. The driving force behind Ableton is
          our passion for what we make, and the people we make it for.
        </p>
      </template>
    </TextBlock>
    <ImageBlock></ImageBlock>
    <TextBlock
      title="We are more than 350 people from 30 different countries divided between our headquarters in Berlin and our offices in Los Angeles and Tokyo."
    >
      <template #text>
        <p>
          Most of us are active musicians, producers, and DJs, and many of us use Live and Push
          every day. We come from a wide range of cultural and professional backgrounds. Some of us
          have PhDs, some are self-taught, and most of us are somewhere in between. What connects us
          is the shared belief that each of us has the skills and knowledge to contribute to
          something big: helping to shape the future of music culture.
        </p>
      </template>
    </TextBlock>
    <ImageBlock></ImageBlock>
    <TextBlock
      title="We believe it takes focus to create truly outstanding instruments. We only work on a few products and we strive to make them great."
    >
      <template #text>
        <p>
          Rather than having a one-size-fits-all process, we try to give our people what they need
          to work their magic and grow. We’ve learned that achieving the best results comes from
          building teams that are richly diverse, and thus able to explore problems from a wider set
          of perspectives. We don’t always agree with each other, but opinion and debate are valued
          and openly encouraged.
        </p></template
      ></TextBlock
    >
    <ImageBlock></ImageBlock>
    <TextBlock
      title="We’re passionate about what we do, but we’re equally passionate about improving who we are."
    >
      <template #text>
        <p>
          We work hard to foster an environment where people can grow both personally and
          professionally, and we strive to create a wealth of opportunities to learn from and with
          each other.
        </p>
        <p>
          Alongside an internal training program, employees are actively supported in acquiring new
          knowledge and skills, and coached on applying these in their daily work. In addition,
          staff-organized development and music salons are a chance to discuss new technologies,
          production techniques and best practices.
        </p>
      </template>
    </TextBlock>
    <ImageBlock></ImageBlock>
  </div>
</template>

<script>
import TextBlock from '@/components/common/TextBlock.vue';
import ImageBlock from '@/components/common/ImageBlock.vue';

export default {
  components: {
    TextBlock,
    ImageBlock,
  },
};
</script>

<style scoped lang="scss">
.title-link {
  text-decoration: none;
  color: var(--color-text-link-primary);
}
</style>
