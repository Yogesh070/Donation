<template>
  <div class="top">
    <div class="condolence">
      <h1>Our Deepest Sympathy</h1>
      <div>
        <img src="../assets/pngwave.png" alt="diyo" class="left-lamp" />
        <img :src="image" alt="picture" id="pp" />
        <img src="../assets/pngwave.png" alt="diyo" class="right-lamp" />
      </div>

      <h2>Mr.{{ name }}</h2>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde, quo
        aliquid recusandae rem voluptates at nihil provident quos dolores
        perspiciatis et! Magni ipsa aspernatur nulla sapiente, deleniti repellat
        sequi in!
      </p>
      <h2>Late {{ name }}</h2>
      <p>
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Corrupti, nisi
        at? Voluptate mollitia ipsa, fuga rem facilis recusandae a est, nostrum
        deleniti odit itaque earum quia maiores dolorem fugit minus!
      </p>
      <img src="../assets/curl.svg" alt="curl" class="curl" />
      <h2>Maiti Nepak Society</h2>
      <h2>Pokhara Nepal</h2>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Tonald Drump",
      image:
        "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcRVPTMs2njqG2lMQzTE9mMHDRqzoqtK-B78sA&usqp=CAU",
    };
  },
};
</script>

<style scoped>
.top {
  display: flex;
  justify-content: center;
  min-height: 100vh;
}
.condolence {
  max-width: 1000px;
  text-align: center;
  padding: 0 2rem;
  border: 2px dashed black;
}
p {
  font-size: 20px;
  text-align: center;
}
h1 {
  font-size: 45px;
  margin: 2rem 0;
}
h2 {
  font-size: 30px;
  margin: 2rem 0;
}
img {
  filter: grayscale(100%);
}
.left-lamp {
  height: 245px;
  object-fit: contain;
  width: 228px;
}
.right-lamp {
  height: 245px;
  object-fit: contain;
  width: 228px;
}
.curl {
  width: 170px;
}
#pp {
  height: 350px;
  width: 280px;
  object-fit: cover;
  border: 2px solid black;
}
@media (max-width: 800px) {
  .left-lamp,
  .right-lamp {
    display: none;
  }
}
</style>