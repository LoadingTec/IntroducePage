<template>
  <div>
    <PDFViewer
      :source="url"
      style="height: 100vh; width: 100vw"
      @download="handleDownload"
      :filename="msg"
    />
  </div>
</template>

<script>
import PDFViewer from 'pdf-viewer-vue'
export default {
  name: 'HelloWorld',
  components: {
    PDFViewer,
  },
  props: {
    msg: String
  },
  data() {
    return {
      url: 'https://raw.githubusercontent.com/LoadingTec/IntroducePage/main/docs/锣鼎科技量化业务简介.pdf'
    }
  }
}
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
</style>
