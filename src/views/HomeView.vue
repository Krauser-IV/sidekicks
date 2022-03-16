<template>
  <div class="home">
    <div class="main_wrapper">
      <comingsoon direction="right" />
      <div class="links">
        <a href="https://twitter.com/sidekicksnft" target="_blank" rel="noopener noreferrer">
          <img src="@/assets/images/twitter.svg" alt="twitter Icon" />
        </a>
        <a href="https://www.instagram.com/sidekicksnft/" target="_blank" rel="noopener noreferrer">
          <img src="@/assets/images/instagram.svg" alt="instagram Icon" />
        </a>
        <a href="https://discord.gg/Z5naKug4CP" target="_blank" rel="noopener noreferrer">
          <img src="@/assets/images/discord.svg" alt="Discord Icon" />
        </a>
        <a href="https://opensea.io/SideKicksNFT" target="_blank" rel="noopener noreferrer">
          <img src="@/assets/images/plat2.svg" alt="plat2 Icon" />
        </a>
        <a href="#" target="_blank" rel="noopener noreferrer">
          <img src="@/assets/images/plat1.svg" alt="plat1 Icon" />
        </a>
      </div>
      <main>
        <img
          src="@/assets/images/logo-orange.svg"
          alt="Sidekicks Logo"
          id="box_logo"
        />
        <img
          src="@/assets/images/text-logo.svg"
          alt="Sidekick  nft"
          id="text_logo"
        />
        <h1>SideKicks <span>NFT</span></h1>
      </main>
      <comingsoon direction="left" />
    </div>
    <section>
      <a href="https://discord.gg/Z5naKug4CP" target="_blank" rel="noopener noreferrer"><button>JOIN THE DISCORD</button></a>
    </section>
  </div>
</template>

<script>
import comingsoon from "@/components/comingsoon.vue";

export default {
  name: "HomeView",
  components: { comingsoon },
};
</script>

<style lang="scss" >
.home {
  height: 100vh;
  width: 100vw;
  overflow: hidden;
}
.main_wrapper {
  height: 85vh;
}
main {
  display: flex;
  padding: 40px;
  align-items: center;
  gap: 50px;
  height: 78%;
  width: 100%;
  transform: translateY(-20px);
  h1 {
    font-size: 10vw;
    color: var(--primaryColor);
    font-weight: 900;
    position: relative;
    display: none;
    span {
      position: absolute;
      font-size: 1.5rem;
      top: 40px;
      right: -45px;
    }
  }
  #box_logo {
    width: 40vw;
  }
  #text_logo {
    width: 50vw;
  }
}
section {
  background: var(--bgDark);
  padding: 20px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 15vh;
  button {
    background: var(--bgColor);
    border: none;
    padding: 10px 40px;
    font-size: 2.2rem;
    font-weight: 900;
    border-radius: 50px;
    color: var(--primaryColor);
    cursor: pointer;
  }
}
.links {
  width: 100%;
  height: 10%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-end;
  gap: 20px;
  padding: 20px;
  img {
    width: 30px;
  }
}
@media only screen and (max-width: 800px) {
  .home {
    overflow-y: scroll;
  }
  main {
    flex-direction: column;
    align-items: center;
    justify-content: center;
    transform: translateY(0px);
    gap: 20px;
    #box_logo {
      width: 100%;
    }
    #text_logo {
      width: 100%;
    }
    h1 {
      transform: translateX(-10px);
      font-size: 4rem;
      span {
        top: 0px;
      }
    }
  }
  section {
    button {
      font-size: 1.5rem;
    }
  }
}
</style>
