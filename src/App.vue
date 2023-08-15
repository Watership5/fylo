<script setup>
  import docu from "./assets/icon-document.svg"
  import folder from "./assets/icon-folder.svg"
  import upload from "./assets/icon-upload.svg"
</script>

<template>
  <main class="container">
    <div class="dom-one">
      <img src="https://fylo-data-storage-component-mu.vercel.app/images/logo.svg" alt="logo"/>
      <p aria-label="caption-hook" class="p">
        The <strong>true cloud</strong> storage
      </p>
      <div class="divider">

      </div>
      <div class="btn-container">

        <button>
          <img :src="docu" alt="document-logo"/>
        </button>
        <button>
          <img :src="folder" alt="document-logo"/>
        </button>
        <button>
          <img :src="upload" alt="document-logo"/>
        </button>
      </div>

    </div>
    <div class="slider-container">
      <div class="text-container">
        <p class="text">
          You've used <span>815 GB</span> of your storage
        </p>
        <div class="mask-div">
          <p class="textS">
            185
          </p>
          <span>
            GB Left
          </span>
        </div>
      </div>
      <div class="slider-one">
        <div class="slider-two">
        </div>
      </div>
      <div class="amount">
        <p>
          <span>0</span> GB
        </p>
        <p>
          <span>1000</span> GB
        </p>
      </div>
    </div>
  </main>
</template>

<style>
  @font-face {
    font-family: "Bold";
    src: url("./assets/Raleway-Bold.ttf");
  }
  @font-face {
    font-family: "Reg";
    src: url("./assets/Raleway-Regular.ttf");
  }
  body{
    background-image: url("https://fylo-data-storage-component-mu.vercel.app/images/bg.svg");
    background-repeat: no-repeat;
    background-size: cover;
    height: 100vh;
    overflow: hidden;
    overflow-y: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .p{
    font-family: "Reg";
    color: white;
    letter-spacing: 1px;
  }
  .container{
    display: flex;
    align-items: flex-end;
    justify-content: center;
    gap: 2rem;
  }
  
  .dom-one{
    background-color: hsla(205, 86%, 58%, 1);
    padding: 3rem;
    padding-left: 6rem;
    border-radius: 1rem;
    border-top-left-radius: 8rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    box-shadow: 34px 42px 100px rgb(5 99 167 / 75%);
    padding-right: 6rem;
    padding-bottom: 2rem;
    animation: slideIn 2s ease;
  }
  .divider{
    background-color: hsla(205, 97%, 26%, 1);
    height: 4px;
    width: 100%;
    border-radius: 100px;
    margin-bottom: 1.5rem;
    margin-top: 1rem;
  }
  .btn-container button{
    height: 45px;
    width: 47px;
    border: 1px solid transparent;
    outline: none;  
    cursor: pointer;
    border-radius: 12px;
    box-shadow: 0 6px 4px rgba(12,56,167,.052);
    background: linear-gradient(to bottom, hsl(205,90%,71%), hsl(205,90%,71%));
  }
  .btn-container{
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 1rem;
  }
  .slider-container{
    position: relative;
    background-color: hsla(205, 86%, 58%, 1);
    box-shadow: 34px 42px 100px rgb(5 99 167 / 75%);
    padding: 2rem;
    padding-right: 4rem;
    border-radius: 20px;
    border-top-right-radius: 130px;
    animation: slideLeft 2s ease;
  }
  .text{
    font-family: "Reg";
    color:rgba(255,255,255,0.6);
  }
  .text span{
    color: white;
    font-family: "Bold";
  }
  .slider-one{
    background-color: hsla(205, 97%, 26%, 1);
    height: 30px;
    width: 37rem;
    border-radius: 100px;
    position: relative;
    margin-top: 1rem;
    box-shadow: 0 2px 4px rgba(12,55,167,.35);
  }
  .slider-two{
    background: linear-gradient(to right,#FFA197 0%,  #FF4A95 100% );
    height: 19.5px;
    border-radius: 100000px;
    margin-top: -1rem;
    position: relative;
    width: 85%;
    opacity: 0;
    left: 6px;
    top: 5px;
    animation: slide 3s ease;
    animation-delay: 2s;
    transform-origin: left;
    animation-fill-mode: forwards;
  }
  .slider-two::after{
    content: '';
    background-color: white;
    height: 0.9rem;
    width: 0.9rem;
    border-radius: 50%;
    position: absolute;
    right: 3px;
    top: 2.5px;
  }
  .text-container{
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .amount{
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-family: "Bold";
    color: white;
    opacity: 0.6;
  }

  .textS{
    background: linear-gradient(to right,#FFA197,  #FF4A95 );
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    font-size: 40px;
  }
  .textS::after{
    content: '';
    background-color: white;
    position: absolute;
    height: 2rem;
    width: 2rem;
    bottom: -15px;
    right: -0.05rem;
    clip-path: polygon(0 0, 100% 0, 100% 100%);
    box-shadow: 0 2px 4px rgba(12,55,167,.35);

  }

  .mask-div{
    font-family: "Bold";
    animation: slideInT 2s ease;
    z-index: 2;
    position: absolute;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 0.5rem;
    right: 3.5rem;
    top: -3rem;
    border-radius: 10px;
    font-size: 40px;font-family: "Bold";
    width: 10rem;
    height: 5rem;
    position: absolute;
    right: 3.5rem;
    top: -3rem;
    border-radius: 10px;
    font-size: 30px;
    background: white;
  }
  .mask-div span{
    color: hsla(205, 86%, 58%,1);
    font-size: 14px;
    text-transform: uppercase;
  }

  @keyframes slideIn{
    from{
      transform: translateY(-500px);
    }
    to{
      transform: translateY(0px);
    }
  }
  @keyframes slideInT{
    from{
      transform: translateY(1000px);
    }
    to{
      transform: translateY(0px);
    }
  }
  
  @keyframes slideLeft {
    from{
      transform: translateX(500px);
    }
    to{
      transform: translateX(0px);
    }
  }
  @keyframes slide {
    from{
      width: 0px;
      opacity: 0;
    }
    to{
      width: 85%;
      opacity: 1;
    }
  }
</style>
