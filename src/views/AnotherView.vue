<template>
  <div class="another">
    <h1>This is another page</h1>
    <!--     <p>Coming from (referrer): {{ myvar }}</p> -->
  </div>
</template>

<script>
export default {
  name: "AnotherView",
  data() {
    return {
      myvar: "",
    };
  },
  mounted() {
    console.log("document.referrer", document.referrer);
    this.myvar = document.referrer;

    // Accessing the document content and referrer
    this.documentContent = document.documentElement.outerHTML;
    this.documentReferrer = document.referrer;

    // Printing the document content and referrer to the console
    //console.log("Document Content:", this.documentContent);
    console.log(" - - Document Referrer:", this.documentReferrer);
    //console.log("document:", document);
    //console.log("document.referrer:", document.referrer);
  },
};
</script>
