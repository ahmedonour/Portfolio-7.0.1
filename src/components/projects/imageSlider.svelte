<script>
    export let images = [
    //   "https://via.placeholder.com/600x400?text=Image+1",
    //   "https://via.placeholder.com/600x400?text=Image+2",
    //   "https://via.placeholder.com/600x400?text=Image+3",
    //   "https://via.placeholder.com/600x400?text=Image+4"
    // "/show1.png",
    //   "/show2.png",
    //   "https://via.placeholder.com/600x400?text=Image+3",
    //   "https://via.placeholder.com/600x400?text=Image+4"
    ];
    let currentImageIndex = 0;
  
    function nextImage() {
      currentImageIndex = (currentImageIndex + 1) % images.length;
    }
  
    function previousImage() {
      currentImageIndex = (currentImageIndex - 1 + images.length) % images.length;
    }
  </script>
  
  <div class="image-slider">
    <!-- svelte-ignore a11y-img-redundant-alt -->
    <img src={images[currentImageIndex]} alt="Slider Image" />
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
    .fa-arrow-left{
        position: relative;
        left: -7rem;
        top: -9rem;
    }
    .fa-arrow-right{
        position: relative;
        right: -7rem;
        top: -9rem;
    }
    .controls button {
      margin: 0 10px;
      background: transparent;
      border: none;
      font-size: 2rem;
      color: var(--clr-Black);
    }
  </style>
  