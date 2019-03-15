<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>Redirecting you to the available Instabot Server, Please Wait</p>
    <img class="redirect" src="../assets/redirect.gif">
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  created: function() {
    let urls = ['https://9a25977e.ngrok.io'];
    
    urls.forEach((url) => {
      console.log(url);
      this.$http.get(url + '/api/welcome')
      .then(response => {
        if (response && response.status == 200) {
          window.location.href = url;
        }
      })
      .catch(response => {});  
    });
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.redirect {
  max-width: 100%;
}
</style>
