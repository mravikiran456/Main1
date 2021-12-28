<template>
    <div className="home-container">
        <div className="home-content">
          <h1 className="home-heading">Treat Your Self</h1>
          <img
            src="~assets/shopp.jpg"
            alt="clothes that get you noticed"
            className="home-mobile-img"
          />
          <p className="home-description">
            Life isn't perfect but your outfit can be.Clothes are just like a friends you want quality not quantity.Get the best offers in the quality products.
            So,celebrate the seasons new and exciting fashion in your own way.


          </p>
          <q-btn color="black" text-color="white" label="Shop Now" class="shop-now-button" @click="$router.replace('/Product')"/>  
        </div>
        <img
        src="~assets/shopp.jpg"
          alt="clothes that get you noticed"
          className="home-desktop-img"
        />
      </div>
</template>
<style>
.home-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin: auto;
  padding-top: 10px;
  padding-bottom: 50px;
  width: 90%;
  max-width: 1110px;
  
}

@media screen and (min-width: 768px) {
  .home-container {
    flex-direction: row;
    justify-content: space-between;
    padding-top: 96px;
  }
}

.home-content {
  display: flex;
  flex-direction: column;
  align-items: center;
}

@media screen and (min-width: 768px) {
  .home-content {
    align-items: flex-start;
  }
}

.home-mobile-img {
  width: 206px;
}

@media screen and (min-width: 768px) {
  .home-mobile-img {
    display: none;
  }
}

.home-desktop-img {
  width: 50%;
  max-width: 450px;
  margin-left: 85px;
}

@media screen and (max-width: 767px) {
  .home-desktop-img {
    display: none;
  }
}

.home-heading {
  color: #1e293b;
  font-family: 'Roboto';
  font-weight: bold;
  font-size: 30px;
  line-height: 1.2;
  text-align: center;
}

@media screen and (min-width: 768px) {
  .home-heading {
    font-size: 46px;
    text-align: left;
  }
}

.home-description {
  font-family: 'Roboto';
  margin-top: 36px;
  font-size: 14px;
  line-height: 28px;
  color: #64748b;
  margin-bottom: 0px;
  text-align: center;
}

@media screen and (min-width: 768px) {
  .home-description {
    font-size: 18px;
    margin-top: 0px;
    text-align: left;
  }
}

.shop-now-button {
  padding-top: 12px;
  padding-bottom: 12px;
  margin-top: 20px;
  cursor: pointer;
  outline: none;
}

@media screen and (min-width: 768px) {
  .shop-now-button {
    width: 150px;
    font-size: 16px;
  }
}
</style>