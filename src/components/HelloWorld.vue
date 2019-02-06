<template>
  <div>
    <h1>{{ nama }}</h1>
    <input type="text" v-model="nama">
    <br><br>
    Nilai : {{ nilai }}
    <br>    
    <h2>{{ soal1 }}</h2>
    <input type="radio" name="jawaban1" :disabled="checked"> Jl.Solontongan No.13
    <input type="radio" name="jawaban1" :disabled="checked"> Jl.BKR No.45
    <input type="radio" name="jawaban1" :disabled="checked" @click="benar"> Jl.Kliningan No.06
    <h2>{{ soal2 }}</h2>
    <input type="radio" name="jawaban2" :disabled="checked2" @click="benar2"> RPL
    <input type="radio" name="jawaban2" :disabled="checked2"> TKJ
    <input type="radio" name="jawaban2" :disabled="checked2"> MM
    <h2>{{ soal3 }}</h2>
    <input type="radio" name="jawaban3" :disabled="checked3"> Biru
    <input type="radio" name="jawaban3" :disabled="checked3" @click="benar3"> Hijau
    <input type="radio" name="jawaban3" :disabled="checked3"> Merah
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      nama: 'Nama',
      nilai: 0,
      soal1: '1. Dimanakah Alamat SMKN 4 Bandung?',
      soal2: '2. Di SMKN 4,Jurusan apa yang mempelajari tentang Software?',
      soal3: '3. Siswa RPL(Rekayasa Perangkat Lunak) Endemik dengan warna apa di SMKN 4?'
    }
  },
  methods:{
    benar(){
      this.nilai += 1,
      this.checked = true
    },
     benar2(){
      this.nilai += 1,
      this.checked2 = true
    },
     benar3(){
      this.nilai += 1,
      this.checked3 = true
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
