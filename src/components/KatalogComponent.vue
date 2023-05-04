<template>
  <div>
    <h1>Гав</h1>
    <div class='boxcard'>
      <v-popup />
      <div v-for='computer in computers' :key='computer.id'>
        <div class='card'>
          <a> KASUMOV PLAYER </a>
          <img :src='computer.image' alt='RTX4090' style='width:100%' id='k1'>
          <p>Игровой Компьютер</p>
          <div class='opisanie'>
            <a href='#'>{{ computer.gpu }}</a>
            <a href='#'>{{ computer.cpu }}</a>
            <a href='#'>{{ computer.mb }}</a>
            <a href='#'>{{ computer.bp }}</a>

            <button class="v-popup-item__show-info" @click="showPopupinfo">
              Жмяк</button>
          </div>
          <div class='price'>{{ computer.price }} рублей</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'KatalogComponent',
  data () {
    return {
      computers: [{
        id: 1,
        cpu: 'Процессор: i5-10400f',
        gpu: 'Видеокарта: RTX 3060',
        mb: 'Материнская плата: MSI B460',
        bp: 'Блок питания: Cheiftec 750v 80+ gold',
        price: 120000,
        image: 'https://digital-razor.ru/upload/iblock/915/915d4e0bb38158b4360e7368f01f95c1.png'
      },
      {
        id: 2,
        cpu: 'Процессор: i5-11600f',
        gpu: 'Видеокарта: RTX 3070TI',
        mb: 'Материнская плата: MSI B560',
        bp: 'Блок питания: Cheiftec 750v 80+ gold',
        price: 80000,
        image: 'https://digital-razor.ru/upload/iblock/915/915d4e0bb38158b4360e7368f01f95c1.png'
      },
      {
        id: 3,
        cpu: 'Процессор: i7-12700f',
        gpu: 'Видеокарта: RTX 3080',
        mb: 'Материнская плата: MSI B660',
        bp: 'Блок питания:Cheiftec 750v 80+ gold',
        price: 60000,
        image: 'https://digital-razor.ru/upload/iblock/915/915d4e0bb38158b4360e7368f01f95c1.png'
      },
      {
        id: 4,
        cpu: 'Процессор: i9-12900f',
        gpu: 'Видеокарта: RTX 3080',
        mb: 'Материнская плата: MSI B660',
        bp: 'Блок питания: Cheiftec 750v 80+ gold',
        price: 70000,
        image: 'https://digital-razor.ru/upload/iblock/915/915d4e0bb38158b4360e7368f01f95c1.png'
      },
      {
        id: 5,
        cpu: 'Процессор: i9-12900f',
        gpu: 'Видеокарта: RTX 3080',
        mb: 'Материнская плата: MSI B660',
        bp: 'Блок питания: Cheiftec 750v 80+ gold',
        price: 90000,
        image: 'https://digital-razor.ru/upload/iblock/915/915d4e0bb38158b4360e7368f01f95c1.png'
      },
      {
        id: 6,
        cpu: 'Процессор: i9-12900f',
        gpu: 'Видеокарта: RTX 3080',
        mb: 'Материнская плата: MSI B660',
        bp: 'Блок питания: Cheiftec 750v 80+ gold',
        price: 40000,
        image: 'https://digital-razor.ru/upload/iblock/915/915d4e0bb38158b4360e7368f01f95c1.png'
      }
      ]
    }
  }

}
</script>

<style>
* {
  margin: 0;
}

.boxcard {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  justify-items: center;
}

.card {
  box-shadow: -6px 10px 20px 0 pink;
  max-width: 300px;
  position: relative;
  margin-top: 10%;
  text-align: center;
  font-family: arial;

}

.price {
  color: grey;
  font-size: 22px;
}

.opis {
  padding: 12px;
  color: orange;
  background-color: rgb(15, 15, 15);
  text-align: center;
  width: 92%;
  font-size: 20px;
  font-weight: bolder;
}

p {
  color: rgb(0, 0, 0);
  font-family: Verdana;
}

.tow {
  color: rgb(0, 0, 0);
}

.card:hover {
  box-shadow: -2px 4px 100px purple;

}

.opisanie {
  padding-left: 5px;
  text-align: left;
  line-height: 32px;
  display: flex;
  flex-direction: column;
}

h3 {
  color: white;

}
</style>
