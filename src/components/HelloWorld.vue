<template>
  <div>
    <PDFViewer
      :source="url"
      style="height: 100vh; width: 100vw"
      @download="handleDownload"
      :filename="fileName"
      :loading-text="loadingText"
      :rendering-text="renderingText"
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
      url: '锣鼎科技量化业务简介.pdf',
      loadingText:'加载文件中......',
      fileName:'锣鼎科技量化业务简介',
      renderingText:'正在为您加速渲染中......'
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
