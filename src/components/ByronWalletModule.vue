<template>
  <section
    id="byron-dex-module"

  >
    <div class="container">
      <div class="row">
        <div class="col-sm-12 col-md-7 order-1">
          <h1>
            Bynet Wallet
          </h1>
          <p>
            Bynet Wallet is an HD native wallet for Cardano that allows users to
            securely store, manage and swap their crypto assets. Send and
            receive tokens on our mobile app. Trade with control over your
            portfolio with a user-friendly design and best-quality security.
          </p>
          <div class="buttons d-flex flex-column flex-sm-row">
            <a
              class="btn btn-primary p-2"
              target="_blank"
              href="https://discord.gg/8kWBQPXwAH"
              >Join us on Discord</a
            >
            <button class="btn btn-primary p-2" @click="$router.push('wallet')">
              Read more
            </button>
          </div>
        </div>
        <div
          class="col-sm-12 col-md-4 offset-md-1 offset-background order-md-1"
        />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ByronDexModule',
};
</script>

<style lang="scss" scoped>
#byron-dex-module {
  padding: 0 15px 80px 15px;

  .offset-background::before {
    content: '';
    background-image: url('../assets/iphone_wallet.png');
    background-repeat: no-repeat;
    background-position: top center;
    background-size: contain;
    width: 100%;
    height: 400px;
    display: block;
    position: absolute;
  }

  h1 {
    font-size: 42px;
    text-align: left;
    margin-top: 10px;
    word-break: break-word;
  }

  p {
    margin-top: 22px;
    text-align: left;
    color: #000;
    font-size: 1rem;
  }

  .buttons {
    .btn {
      padding: 15px 40px !important;
      border-radius: 12px;
      font-weight: 700;

      &:nth-child(2) {
        margin-left: 12px;
      }

      &:hover {
        color: white;
      }
    }
  }

  @media (max-width: 767px) {
    .offset-background {
      height: 300px;
      &::before {
        width: 95%;
        height: 100%;
      }
    }

    .buttons {
      justify-content: space-around;
      margin-bottom: 10px;
    }

    .reverse {
      flex-direction: reverse;
    }
  }

  @media (max-width: 576px) {
    .buttons {
      .btn {
        &:nth-child(2) {
          margin-left: 0px;
          margin-top: 10px;
        }
      }
    }
  }

  @media (min-width: 1200px) {
    h1 {
      font-size: 58px;
      margin-top: 50px;
    }
  }
}
</style>
