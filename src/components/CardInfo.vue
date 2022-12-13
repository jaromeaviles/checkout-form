<template>
  <div class="col-12 col-lg-7">
    <div class="card-container">
      <h1>Payment Information</h1>
      <div class="card-information">
        <div class="card-image-container">
          <img :src="require('@/assets/card.jpeg')" alt="card" />
          <div class="overlay">
            <div class="text-overlay-header">
              <img :src="require('@/assets/chip.png')" alt="chip" />
              <div class="overlay-card-number">
                <p>&#x23; &#x23; &#x23; &#x23;</p>
                <p>&#x23; &#x23; &#x23; &#x23;</p>
                <p>&#x23; &#x23; &#x23; &#x23;</p>
                <p>&#x23; &#x23; &#x23; &#x23;</p>
              </div>
              <div class="card-personal-information">
                <div class="card-holder">
                  <h3>Card Holder</h3>
                  <p>FULL NAME</p>
                </div>
                <div class="expiration">
                  <h3>Expires</h3>
                  <p>MM/YY</p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- Form -->
        <form>
          <div class="mb-3">
            <label for="name" class="form-label">Name on card</label>
            <input
              type="text"
              class="form-control"
              id="name"
            />
          </div>
           <div class="mb-3">
            <label for="cardNumber" class="form-label">Card number</label>
            <input
              type="text"
              class="form-control"
              id="cardNumber"
            />
          </div>
          <div class="row g-3 align-items-center card-details">
            <div class="col-auto">
            <label for="expirationDate" class="form-label">Expiration date</label>
            <input
              type="text"
              class="form-control"
              id="expirationDate"
              placeholder="Month"
            />
            </div>
            <div class="col-auto">
            <label for="year" class="form-label">&nbsp;</label>
            <input
              type="text"
              class="form-control"
              id="year"
              placeholder="Year"
            />
            </div>
             <div class="col-auto">
            <label for="cvc" class="form-label">CVC</label>
            <input
              type="text"
              class="form-control"
              id="cvc"
            />
            </div>
          </div>
          <div class="price-container">
            <p>950 USD</p>
          </div>
          <button type="submit" class="btn btn-success">Confirm payment</button>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
h1 {
  font-size: 18px;
  margin-bottom: 10px;
  text-align: left;
}
.card-information {
  background-color: white;
  padding: 30px;
  border-radius: 5px;
  box-shadow: rgba(0, 0, 0, 0.12) 0px 1px 3px, rgba(0, 0, 0, 0.24) 0px 1px 2px;
  .card-image-container {
    position: relative;
    width: 245px;
    margin: 0 auto;
    @media only screen and (min-width: 992px) {
      width: 340px;
    }
    > img {
      object-fit: cover;
      width: 100%;
      border-radius: 15px;
      box-shadow: rgba(50, 50, 93, 0.25) 0px 30px 60px -12px,
        rgba(0, 0, 0, 0.3) 0px 18px 36px -18px;
    }
    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.5);
      padding: 15px;
      border-radius: 15px;
      img {
        width: 40px;
        height: auto;
        @media only screen and (min-width: 992px) {
          width: 50px;
        }
      }
      .text-overlay-header {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        height: 100%;
        color: white;

        .overlay-card-number {
          display: flex;
          flex-direction: row;
          justify-content: space-between;
          width: 100%;
          @media only screen and (min-width: 992px) {
            width: 280px;
          }
          p {
            font-size: 17px;
            margin-bottom: 0;
            letter-spacing: -1px;
            @media only screen and (min-width: 992px) {
              font-size: 22px;
            }
          }
        }
        .card-personal-information {
          display: flex;
          justify-content: space-between;
          h3 {
            font-size: 10px;
            opacity: 0.8;
            font-weight: 400;
            @media only screen and (min-width: 992px) {
              font-size: 12px;
            }
          }
          p {
            font-size: 12px;
            margin-bottom: 0;
            @media only screen and (min-width: 992px) {
              font-size: 14px;
            }
          }
        }
      }
    }
  }

  form {
    text-align: left;
    margin-top: 20px;

    .price-container {
        text-align: right;
        margin: 20px 0;

        p {
            font-weight: bolder;
        }
    }

    button {
        width: 100%;
    }
  }
}
</style>
