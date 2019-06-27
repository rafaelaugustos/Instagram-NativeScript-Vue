<template>
  <StackLayout class="post">
    <FlexboxLayout class="post__profile">
      <StackLayout class="post__imgProfile">
        <Image
          src="~/assets/images/rafael.jpg"
          style="width: 100%"
        />
      </StackLayout>
      <Label text="rafaelaugusto.me" />
    </FlexboxLayout>
    <Image 
      class="post__image"
      :src="Image" 
    />
    <FlexboxLayout class="post__desc">
      <Label 
        textWrap
        text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla libero mi, placerat eu lacus vel, vestibulum varius ipsum." 
      />
    </FlexboxLayout>
  </StackLayout>
</template>

<script>
  export default {
    props: {
      Image: String
    }
  }
</script>

<style lang="scss" scoped>
  .post{
    margin-top: 20;

    &__profile{
      padding: 0 10 10 10;

      Label{
        margin-left: 10;
        font-size: 13;
        font-weight: 500;
      }
    }

    &__imgProfile{
      width: 35;
      height: 35;
      border-radius: 100;
      overflow: hidden;
    }

    &__desc{
      padding: 10;
      
      Label{
        font-size: 12;
      }
    }
  }
</style>
