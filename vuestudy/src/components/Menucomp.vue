<template>
    <div class="menu">
      <div class="nav">
        <h1>
          <router-link to="/vueblog">BYSEONG</router-link>
        </h1>
        <div>
          <router-link to="/post" @click="$emit('menuClick')">Blog List</router-link>
        </div>
      </div>
    </div>
</template>
<script>


export default {
  name : 'Menu',
}

</script>

<style>
.menu {
  position: fixed;
  width: 100%;
  box-sizing: border-box;
  z-index: 1000;
  left: 0;
  top: 50px;
}
.menu>div {
  border: 0.13rem solid #888;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #fff;
  width: calc(100% - 160px);
  padding: 15px;
  border-radius: 1.3rem;
  text-align: center;
  margin: 0 auto;
  box-shadow: rgba(60, 64, 67, 0.3) 0px 1px 2px 0px, rgba(60, 64, 67, 0.15) 0px 2px 6px 2px;
}
.menu>div>h1>a {
  box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px, rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
  border: 0.15rem solid #444;
  border-radius: 10rem;
  color : #444;
  padding : 10px;
  font-weight: bold;
  font-size: 18px;
  display: inline-block;
  text-align: left;
  font-family: 'roboto', sans-serif;
}
.menu>div>div {display: flex;flex: 3;justify-content: end;}
.menu>div>div>a {box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px, rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;border: 0.15rem solid #444;color: #444;font-size: 18px;letter-spacing: -0.05em;font-weight: bold;padding: 0.5rem 1.2rem;border-radius: 10rem;}
.menu>div>h1>a:hover,
.menu>div>div>a:hover {color: #fff;background-color: #333;}
.menu>div>div>a:last-child {display: inline-block;margin-left: 50px;}


@media (max-width: 1920px) {
  .menu>div {padding: 10px;}
  .menu>div>div>a,.menu>div>h1>a {font-size: 16px;}
}

@media (min-width: 1500px) and (max-width: 1920px) {
  .menu>div {padding: 10px;width: calc(100% - 200px);}
  .menu>div>div>a,.menu>div>h1>a {font-size: 16px;}
}

@media (min-width: 1440px) and (max-width: 1500px) {
  .menu>div {padding: 10px;width: calc(100% - 200px);}
}
@media (min-width: 1024px) and (max-width: 1440px) {
  .menu>div {padding: 10px;width: calc(100% - 160px);}
}
@media (max-width: 1024px) {
  .menu>div {padding: 10px;width: calc(100% - 80px);}
}
@media (max-width: 768px) {
  .menu {top: 30px;}
  .menu>div {padding: 10px;width: calc(100% - 40px);}
}

</style>