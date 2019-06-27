<template>
  <Page>
    <ActionBar>
      <StackLayout>
        <Image class="logo" src="~/assets/images/logo.png" />
      </StackLayout>
    </ActionBar>

    <ScrollView>
      <StackLayout>
        <Post 
          v-for="(item, index) in posts" 
          :key="index"
          :Image="item.Image"
        />
      </StackLayout>
    </ScrollView>
  </Page>
</template>

<script>
  import Post from './Post'

  export default {
    data(){
      return{
        posts: [
          { Image: 'https://thenypost.files.wordpress.com/2018/12/181222-stuy-town.jpg?quality=90&strip=all&w=618&h=410&crop=1' },
          { Image: 'https://etacanadavisa.com.br/main/wp-content/uploads/2018/05/image3-3-830x552.jpg' },
          { Image: 'https://nespy2aub3if2yow3fcm0t5y-wpengine.netdna-ssl.com/files/2013/11/conhe%C3%A7a-londres-635x359.jpg' },
          { Image: 'https://abrilviagemeturismo.files.wordpress.com/2017/12/istock-842960000.jpg?quality=70&strip=info&w=680&h=453&crop=1' }
        ]
      }
    },
    components: { Post }
  }
</script>

<style lang="scss" scoped>
  ActionBar {
    background-color: #f5f5f5;
    color: #ffffff;
  }

  .logo{
    width: 100;
  }

  .message {
    vertical-align: center;
    text-align: center;
    font-size: 20;
    color: #333333;
  }
</style>
