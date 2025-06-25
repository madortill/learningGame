<template>
  <div id="Loader">
    <img 
        class="gif" 
        src="/src/assets/gifs/gif-till.gif" 
        alt="Loading..." 
        className="gif-load"
      />
    <p class="getting-started">מיד מתחילים...</p>
  </div>
</template>

<script>
export default {
  name: "Loader",
  data() {
    return {
    };
  },
};
</script>

<style scoped>
#Loader {
  display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 55vh; 
    background-color: #90e0ef;
    animation: fadeOut 4.5s ease-in-out forwards; 
    overflow: hidden;
}

.gif-load {
  width:25rem;
  height: auto;
  filter: sepia(1) saturate(1000%) hue-rotate(172deg) brightness(0.5);
}

.getting-started {
  font-size: 1.5rem;
  margin-top: 10px;
  font-weight: 700;
  color: #024668;
}

@keyframes fadeOut {
    0% {
      opacity: 1; 
    }
    100% {
      opacity: 0; 
      visibility: hidden; 
    }
  }
  
</style>