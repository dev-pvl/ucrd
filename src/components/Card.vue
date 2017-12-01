<template>
  <div class="wrap">
    <MainHeader></MainHeader>
    <div class="card">
        <img v-bind:src="imgSrc" class="card__img">
        <h3 class="card__name">{{name}}</h3>
        <h4 class="card__position">{{position}}</h4>
        <button class="card__btn" type="button" name="button">{{btnText}}</button>
        <p class="card__description">{{description}}</p>
        <p class="card__location">Location</p>
        <p class="card__location--user">{{location}}</p>
    </div>
    <Settings v-if="showSettings"></Settings>
  </div>
</template>

<script>
import MainHeader from '@/components/Header';
import Settings from '@/components/Settings';

export default {
  components: {
    MainHeader,
    Settings,
  },
  name: 'card',
  data() {
    return {
      imgSrc: 'static/img/alice.jpg',
      name: 'Alice Williams',
      position: 'Designer and team leader in VoltTechs',
      btnText: 'My YouTube channel!',
      description: 'Consultant by day, Urban Adventurer by night. Alice is an ambitious young New Yorker who enjoys writing her life story as though she’s the protagonist of a novel, observing the world from as many angles as possible, and helping other people achieve their dreams. In all imagine ways. When Alice isn’t running around Manhattan tasked with several missions in her planet, you might find her at Deloitte Consulting where she is a Business Analyst or around New York University where she is an active alumna. She also runs career and lifestyle blog: alicemanhattan-go.com',
      location: 'Kiev, Ukraine',
      showSettings: false,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .card {
    --cardColor: #372c39;
    --btnText: #fff;
    --btnWidth: 150px;
    --btnHeight: 30px;
    --btnColor: #8d26c6;
  }
  .card {
    box-sizing: border-box;
    padding: 25px 0;
    margin: auto;
    width: 720px;
    height: 380px;
    background: #fff;
    border-radius: 3px;
    color: var(--cardColor);
  }
  .card__img {
    margin: 0 25px 25px 25px;
    float: left;
    border-radius: 100%;
    width: 320px;
    height: 320px;
  }
  .card__name {
    font-size: 26px;
    margin:0 0 10px 0;
  }
  .card__position {
    font-size: 14px;
    margin: 0;
  }
  .card__btn {
    width: var(--btnWidth);
    height: var(--btnHeight);
    color: var(--btnText);
    display: block;
    margin: 15px 0;
    background: var(--btnColor);
    border: none;
    box-shadow: 0;
    border-radius: 3px;
  }
  .card__description {
    font-size: 14px;
  }
  .card__location {
    font-size: 12px;
    font-weight: 700;
    margin-bottom: 0;
  }
  .card__location--user {
    font-size: 12px;
    margin: 0;
  }
</style>
