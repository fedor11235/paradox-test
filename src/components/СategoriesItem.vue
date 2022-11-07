<template>
  <div class="category">
    <div class="category__more category__arrow-down" @click="handlerMore"></div>
    <span class="category__title">{{title}}</span>
    <span class="category__suptitle">{{suptitle}}</span>
    <div class="category__toolbar">
      <img class="category__toolbar__item" src="@/assets/img/editing.png" alt="editing" />
      <img class="category__toolbar__item" src="@/assets/img/delete.png" alt="delete" />
      <img class="category__toolbar__item" src="@/assets/img/move.png" alt="move" />
    </div>
  </div>
</template>

<script>

export default {
  name: 'СategoriesItem',
  props: {
    title: {
      type: String,
      required: true
    },
    suptitle: {
      type: String,
      default: ''
    }
  },
  methods: {
    handlerMore(e) {
      if(e.target.className.includes('category__arrow-down')) {
        e.target.classList.remove('category__arrow-down')
        e.target.classList.add('category__arrow-up')
      } else {
        e.target.classList.remove('category__arrow-up')
        e.target.classList.add('category__arrow-down')
      }
    }
  }
}
</script>

<style lang="scss">
.category {
  position: relative;
  display: flex;
  align-items: center;
  padding: 0 16px;
  height: 48px;
  outline: 1px solid #DFE4EF;
  &__more {
    // position: absolute;
    // top: 13px;
    // left: 16px;
    margin-right: 14px;
    min-width: 22px;
    min-height: 22px;
    outline: 1px solid #DFE4EF;
    border-radius: 50%;
    cursor: pointer;
  }
  &__arrow-down {
    background-image: url(@/assets/img/arrow-down.png);
    background-position: center;
    background-repeat: no-repeat;
  }
  &__arrow-up {
    background-image: url(@/assets/img/arrow-up.png);
    background-position: center;
    background-repeat: no-repeat;
  }
  &__title {
    font-family: 'Fira Sans';
    font-style: normal;
    font-weight: 500;
    font-size: 15px;
    line-height: 108%;
    margin-right: 15px;

    white-space: nowrap;
  }
  &__suptitle {
    max-width: 718px;
    font-family: 'Fira Sans';
    font-style: normal;
    font-weight: 400;
    font-size: 11px;
    line-height: 108%;
    color: #8E9CBB;

    overflow: hidden;
    white-space: nowrap;
    text-overflow: clip;
  }
  &__toolbar {
    position: absolute;
    right: 0;
    background-color: white;
    box-shadow: -10px 0 10px 0 white;
    &__item {
      padding: 0 16px;
      cursor: pointer;
    }
  }
}
</style>
