<script>
  let dateStart = new Date('2019-11-06').getTime();
  let dateNow = new Date().getTime();
  let dateEnd = new Date('2020-07-06').getTime();
  let diff = dateEnd - dateNow;
  let days = Math.round(diff/(1000*60*60*24));
  let stop = false;

  const total = dateEnd - dateStart;
  const offset = dateNow - dateStart;
  const percent = (offset / total) * 100;
  const seconds = percent * 10000 / 100;

  setTimeout(() => {
    stop = true;
  }, seconds);
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');

  :global(*) {
    box-sizing: border-box;
  }

  :global(body) {
    font-family: 'Pacifico', cursive;
    margin: 0;
    padding: 0;
    color: white;
  }

  .App {
    background: rgba(24,96,179,0.5);
    position: absolute;
    bottom: 0;
    top: 0;
    width: 100%;
    padding: 1em;
  }
  .App-container {
    display: grid;
    grid-template-columns: minmax(auto,1280px);
    justify-content: center;
    align-items: center;
  }
  .App-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .App-content img {
    width: 65%;
    height: auto;
  }

  h1 {
    color: #f8cf2d;
    font-size: 55px;
    margin: 0;
    padding: 0;
    letter-spacing: 2px;
    text-shadow: 6px 6px 0px rgba(0,0,0,0.2);
  }
  p {
    font-size: 40px;
    margin: 0;
    padding: 0;
    letter-spacing: 1.2px;
    text-shadow: 3px 3px 0px rgba(0,0,0,0.2);
  }
  figure {
    margin: 0;
    padding: 0;
    text-align: right;
  }

#myBaby {
  position: fixed;
  right: 0;
  bottom: 0;
  min-width: 100%;
  min-height: 100%;
}

@media (max-width: 534px) {
  .App-title {
    text-align: center;
  }
  h1 {
    font-size: 35px;
  }
  p {
    font-size: 25px;
  }
  .App-container {
    height: 100%;
  }
  .App-content {
    display: block;
  }
  img {
    width: 50%;
  }
  figure {
    display: none
  }
}

  svg #path2 {
    animation: pregnant 10s linear forwards;
  }
  svg.stop #path2 {
    animation-play-state: paused;
  }
  @keyframes pregnant {
    100% {
      d: path("m 39.9,27.3 -8.5,-0.6 c 0,4.8 -9.771462,6.998901 -9.771462,10.798901 0,2.7 1.871462,3.401099 1.871462,3.401099 0,0 -8.259165,1.742921 -8.259165,10.142921 C 15.240835,57.742921 20.9,61.9 27.2,61.9 h 10.3 c 0,0 0.7,-2 -0.6,-9.1 -2.5,-13.9 7.6,-11.6 3,-25.5");
    }
  }


</style>

<video autoplay muted loop id="myBaby">
  <source src="https://arepa.s3.amazonaws.com/baby-bg.mp4" type="video/mp4">
</video>

<div class="App">
  <div class="App-container">
    <div class="App-content">
      <div class="App-title">
        <h1>Oscar Barajas Jr.</h1>
        {#if days === 0}
          <p>¡He nacido! 👶 6/7/20</p>
        {:else}
          <p>¡He nacido! 👶 6/7/20</p>
        {/if}
      </div>
      <figure>
        <img src="https://arepa.s3.amazonaws.com/bgbebeloper.png" alt="Oscar Barajas Jr.">
      </figure>
    </div>
  </div>
</div>
