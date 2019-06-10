<template>
    <q-page>
     <q-list bordered>
         <q-item>
          {{post.data.naziv_roda}}
         </q-item>
     </q-list>
    </q-page>
</template>

<script>
export default {
  loadData () {
    this.$axios.get('http://193.198.97.14:8000/api/rodovi/1/')
      .then((response) => {
        alert(response.data.naziv_roda)
      })
      .catch((error) => {
        console.log(error)
      })
  },
  data () {
    return {
      posts: []
    }
  }
}
</script>
