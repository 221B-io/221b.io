<template lang="pug">
  .container(style="background:#FFF;padding:0px;border-radius:15px;max-width:1000px;margin-bottom:30px;")
    //- header
    header
      h1(style="font-size:3em;").text-center.py-5
        strong 221B

    //- banner
    section.banner.px-5
      h2.px-5
        WordSwapper
      ul.actions.special.px-5.text-right(style="justify-content:inherit;")
        li
          a(href="mailto:inquiries@221b.io").button Contact Us

    //- Our values
    //- section#three.wrapper.style2.spotlight
    //-   .content(style="width:70%")
    //-     .inner
    //-       h2 Our Values
    //-       <p class="lead">Make it <strong>good</strong>. Make it <strong>fast</strong>. Make it <strong>robust</strong>. Make it <strong>scalable</strong>. Make it <strong>easy</strong>. Make it <strong>accessible</strong>. Make it <strong>fun to use</strong>.
    //-       <br>Be <strong>transparent</strong>. Be <strong>results-focused</strong>. Be <strong>helpful</strong>. Be <strong>aggressively ethical</strong>.</p>

    //- services
    a(name="services")
    section#one.wrapper.spotlight
      .content
        .inner
          h2 Our Services
          <p class="lead">We offer a wide range of services, fitting with the various expertise of our employees. From training, to strategic advice, to development work, we've got you covered.</p>
      ul.grid-icons(style="border-width:0px")
        li
          .inner
            span.icon.fa-cog.major
            h3 Capacity Building
        li
          .inner
            span.icon.fa-desktop.major
            h3 Product Development
        li
          .inner
            span.icon.fa-signal.major
            h3 Strategy Consultations
        li
          .inner
            span.icon.fa-check.major
            h3 Cleanup

    //- Lives saved
    //- a(name="lives")
    //- section#two.wrapper.style1.spotlight.alt
    //-   .content(style="width:70%")
    //-     .inner
    //-       h2 How many lives can we save?
    //-       <p class="lead">We ask ourselves this question constantly. When there's room for a solution to a serious problem, a solution that could help save or improve lives, you'll find us there.</p>

    //- About the team
    a(name="team")
    section#five.wrapper.special.team
      h2 Our Team
      //- p Praesent dapibus, neque id cursus faucibus, tortor neque ege tas augue, eu vulputate magna eros eu erat. Aliquam erat et volutpat. Nam dui mi, tincidunt quis, accumsan porttitor tempus lorem ipsum dolor sit amet consequat.
      ul.faces
        li
          span.image
            img(src="~static/images/staff/jeff.jpg" alt="Headshot of Jeff Spies")
          h3.mb-0 Jeff Spies
          h5 Principal
          //- p "Aliquam erat et volutpat. Nam dui mi, tincidunt quis, porttitor magna etiam lorem tempus."
          a(href="https://twitter.com/jeffspies").icon
            i.fa.fa-twitter.fa-2x.text-gray
          a(href="https://github.com/jeffspies").icon
            i.fa.fa-github.fa-2x.text-gray
        li
          span.image
            img(src="~static/images/staff/ryan.jpeg" alt="Headshot of Ryan Mason")
          h3.mb-0 Ryan Mason
          h5 Developer
          //- p "Aliquam erat et volutpat. Nam dui mi, tincidunt quis, porttitor magna etiam lorem tempus."
          a(href="https://twitter.com/ryanmasonjar").icon
            i.fa.fa-twitter.fa-2x.text-gray
          a(href="https://github.com/rytiggy").icon
            i.fa.fa-github.fa-2x.text-gray
        li
          span.image
            img(src="~static/images/staff/cam.jpeg" alt="Headshot of Cameron Blandford")
          h3.mb-0 Cameron Blandford
          h5 Developer
          //- p Can't choose a favorite color. Loves seeing theory in practice.
          a(href="https://twitter.com/camblandford").icon
            i.fa.fa-twitter.fa-2x.text-gray
          a(href="https://github.com/cameronblandford").icon
            i.fa.fa-github.fa-2x.text-gray

    //- //- footer with contact info
    a(name="contact")
    Footer
</template>

<script>
import Footer from "~/components/Footer.vue";
import WordSwapper from "~/components/WordSwapper.vue";

export default {
  components: {
    Footer,
    WordSwapper
  }
};
</script>

<style>
.team img {
  width: 200px;
}
ul.grid-icons li {
  border-width: 0px;
}
.wrapper.spotlight > .grid-icons {
  border-width: 0px !important;
}
</style>
