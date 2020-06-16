<script>
  let dateNow = new Date().getTime();
  let dateEnd = new Date('2020-07-06').getTime();
  let diff = dateEnd - dateNow;
  let days = Math.round(diff/(1000*60*60*24));
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
    font-size: 30px;
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
  .App-content {
    display: block;
  }
  img {
    width: 50%;
  }
  figure {
    text-align: center;
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
          <p>¡Ha nacido!</p>
        {:else}
          <p>Días estimados para nacer: {days}</p>
        {/if}
      </div>
      <figure>
        <img src="https://arepa.s3.amazonaws.com/bgbebeloper.png" alt="Oscar Barajas Jr.">
      </figure>
    </div>
  </div>
</div>