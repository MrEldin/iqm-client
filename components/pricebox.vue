<template>
  <div class="price-box rounded" :class="{'primary': primary}">
    <div class="price-box__type">
      <h2>{{price_type}}</h2>
    </div>
    <div class="price-box__price">
      <p v-if="currency">{{currency}}</p>
      <h1>{{price}}</h1>
    </div>
    <div class="price-box__info">
      <h2>PER MONTH</h2>
      <p>{{description}}</p>
    </div>
  </div>
</template>

<script>
  export default {
    name: "pricebox",
    props: {
      primary: {
        type: Boolean,
        default: false
      },
      price_type: {
        type: String,
        default: 'COMPETITIVE'
      },
      price: {
        type: String,
        default: null
      },
      description: {
        type: String,
        required: true,
      },
      currency: {
        type: String,
        default: null
      },
    },
  }
</script>

<style lang="scss">
  .price-box {
    backdrop-filter: blur(30px);
    width: 340px;
    height: 360px;
    background-image: linear-gradient(220deg, rgba(25, 118, 210, 0.60) 10%, rgba(0, 96, 100, 0.60));
    -webkit-box-shadow: 0px 20px 40px 5px rgba(0, 0, 0, 0.25);
    box-shadow: 0px 20px 40px 5px rgba(0, 0, 0, 0.25);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 2px;
    transition: 500ms;
    cursor: pointer;

    &:hover {
      background-image: linear-gradient(220deg,  rgba(0, 96, 100, 0.60) 10%, rgba(25, 118, 210, 0.60));
      backdrop-filter: blur(20px);
    }

    .price-box__type {
      width: 100%;
      display: flex;
      justify-content: center;

      h2 {
        color: white;
        font-size: 24px;
        opacity: 0.69;
      }
    }
    .price-box__price {
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: flex-end;

      p {
        color: white;
        font-size: 24px;
        margin: 0 5px 0 0;
        padding-bottom: 10px;
        font-weight: 600;
        font-family: "Helvetica";
      }

      h1 {
        color: white;
        font-size: 48px;
        font-weight: 600;
        margin: 0;
        padding: 0;
        font-family: "Helvetica";
      }
    }
    .price-box__info {
      width: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;

      h2 {
        text-align: center;
        color: white;
        font-size: 12px;
        margin-bottom: 15px;
        opacity: 0.69;
      }

      p {
        padding: 0 32px;
        color: white;
      }
    }

    &.primary {
      width: 330px;
      height: 400px;
    }
  }
</style>
