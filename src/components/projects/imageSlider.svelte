<script>
    export let images = [];
    let currentImageIndex = 0;
    let slideTimer = null;

    function nextImage() {
      currentImageIndex = (currentImageIndex + 1) % images.length;
    }
  
    function previousImage() {
      currentImageIndex = (currentImageIndex - 1 + images.length) % images.length;
    }
    // const SLIDE_INTERVAL = 1000; // 5 seconds

// let slideTimer = setInterval(() => {
//   nextImage();
// }, SLIDE_INTERVAL);

// $: {
//   clearInterval(slideTimer);
//   slideTimer = setInterval(() => {
//     nextImage();
//   }, SLIDE_INTERVAL);
// }
function startSlideShow() {
    slideTimer = setInterval(() => {
      nextImage();
    }, 3000);
  }

  function stopSlideShow() {
    clearInterval(slideTimer);
    slideTimer = null;
  }

  startSlideShow();
  </script>

  <!-- svelte-ignore a11y-mouse-events-have-key-events -->
  <div class="image-slider"
  on:mouseover={stopSlideShow}
  on:mouseout={startSlideShow}
  >
    <!-- svelte-ignore a11y-img-redundant-alt -->
    <img src={images[currentImageIndex]} alt="Slider Image" 
    on:mouseover={stopSlideShow}
    on:mouseout={startSlideShow}
    />
    <div class="controls">
      <button on:click={previousImage}><i class="fas fa-arrow-left" /></button>
      <button on:click={nextImage}><i class="fas fa-arrow-right" /></button>
    </div>
  </div>
  
  <style>
    .image-slider {
      /* position: relative; */
      width: 100%;
      /* height: 400px; */
      /* overflow: hidden; */
     
      
    }
  
    .image-slider img {
      /* position: absolute;
      top: 0;
      left: 0; */
      border-radius: 1rem;
      width: 100%;
      /* height: 100%;
      object-fit: cover; */
    }
  
    .controls {
      /* top: 90%;
      left: 50%;
      transform: translate(-50%, -90%); */
      display: flex;
      justify-content: center;
    }
    /* .fa-arrow-left{
        position: relative;
        left: -7rem;
        top: -9rem;
    }
    .fa-arrow-right{
        position: relative;
        right: -7rem;
        top: -9rem;
    } */
    .controls button {
      margin: 0 5rem;
      background: transparent;
      border: none;
      font-size: 2rem;
      color: var(--clr-Black);
      cursor: pointer;
    }
  </style>
  