<script setup>
import { ref } from 'vue'
import 'https://kit.fontawesome.com/8078ebeeed.js'
const list = ref([]);
const listshop = ref([]);

const coffeeList =ref([{name:'The Nest Cafe',reviwe:'The Nest Cafe ร้านอาหาร บรรยากาศดีใกล้ชิดธรรมชาติ จัดเต็มทั้งอาหารเหนือ อาหารพื้นเมือง และเครื่องดื่มหลากหลาย ที่นอกจะอิ่มท้องจากอาหาร ยังอิ่มใจกับบรรยากาศท่ามกลางขุนเขา ชมวิวได้รอบ 180 องศา มุมถ่ายรูปเยอะ และมีเมนูเด็ดอย่าง “ฮังเลคากิกับข้าวซอยลอยฟ้า” อาหารเหนือพื้นบ้านแท้ ๆ นอกจากเมนู อาหาร เครื่องดื่มแล้ว ที่นี่ยังมีที่พักอีกด้วย',rate:'101 - 250',open:'9:00-17:30 น',link:'https://www.chillnaid.com/wp-content/uploads/2020/07/thenest-1-12.jpg'},
                       {name:'TEA FAC',reviwe:'ร้านกาแฟโกดังสีดำ ย่านสันติธรรม “TEA FAC.” เริ่มจากโรงคั่วชา Bluemocha แล้วเพิ่มเติมมาด้วยร้านกาแฟคุณภาพดี ราคาน่ารักเริ่มต้นแค่ 37.- เมนูซิกเนเจอร์คือ “Tea Fac” เข้มข้น และหอมมัน เบลนด์ด้วยสูตรเฉพาะ หรือถ้าชอบความสดชื่นต้อง “ชาพีช” ใช้ใบชาอบพีชแท้ ๆ หอมทุกคำที่ดื่ม',rate:'ต่ำกว่า 100',open:'8:00-18:00 น',link:'https://www.hungryfatguy.com/wp-content/uploads/2022/10/20221001_150357.jpg'},
                       {name:'Ristr8to',reviwe:'วันนี้จะมาแนะนำ ร้านกาแฟเชียงใหม่เทพ ๆ ย่านถนนนิมาน ร้านนี้อยู่หน้านิมมานซอยสาม มีลูกค้าเยอะตลอดทั้งวัน ทั้งชาวไทยและชาวต่างชาติ มีเมนูให้เลือกเยอะ มีเมล็ดกาแฟให้เลือกเยอะเช่นกัน วันนี้ได้สั่งเป็น “Dirty” ทางร้านผสมนมได้โอเคมาก ไม่หวาน มัน ๆ กำลังดี ช็อตกาแฟหอม ๆ ใส่ลงไปเข้ากันมาก สายกาแฟไม่ควรพลาดร้านนี้ ทั้งเรื่องรสชาติและบรรยากาศ ควรมาครับ',rate:'ต่ำกว่า 100',open:'7:00-18:00 น',link:'https://www.hungryfatguy.com/wp-content/uploads/2014/04/KNS_1811-650x433.jpg'},
                       {name:'ROAST8RY LAB',reviwe:'ร้านกาแฟดังเชียงใหม่อีกสาขา ที่อยู่ไม่ไกลจากสาขาแรก ที่นั่งเยอะกว่า แต่คนก็เยอะเหมือนเดิม วันนี้ได้สั่งเป็นเครื่องดื่มอย่าง “Blvck & Yellow” เป็นกาแฟดำผสมกับน้ำมะม่วง ท็อปด้วยเนื้อมะม่วงอบแห้ง กาแฟรสละมุนมาก เข้ากันได้ดีกับน้ำมะม่วง แก้วนี้โดนใจมาก อีกแก้วเป็น “Godmother Mocha” กาแฟกับโกโก้เข้มข้น เสิร์ฟมาในทรงกระบอกที่มีส่วนเว้าเป็นหัวกะโหลก รูปทรงเป็นเอกลักษณ์ของทางร้าน รสชาติกลมกล่อมเข้มข้น ดีงามเช่นกัน',rate:'101 - 250',open:'8:00-17:00 น',link:'https://img.wongnai.com/p/400x0/2021/12/19/3ee07b1b221d4d8a8837272d8f67177f.jpg'},
                       {name:'Roxpresso Coffee Craft',reviwe:'ร้านกาแฟในเชียงใหม่ดี ๆ ที่มีความพิถีพิถันมาก หน้าร้านเป็นซอยเล็กนะคะ หาที่จอดรถค่อนข้างยากเลยค่ะ ภายในร้านสวยค่ะ ชอบการตกแต่ง สายฮอปปิงก็มาถ่ายรูปได้นะคะ สำหรับเมนูกาแฟต่าง ๆ ราคาค่อนข้างสูงทีเดียว แต่ดูจากการทำแล้ว เค้าค่อนข้างพิถีพิถันมาก เราว่ากาแฟดีเลยทีเดียว',rate:'101 - 250',open:'9:00-17:30 น',link:'https://www.bloggang.com/data/p/pangeataround/picture/1609586023.jpg'}])

function ntable(name) {   
  const x = {
    shop:name
  }
  
  list.value.splice(x);
  list.value.push(x);

}
function re() {
  window.location.reload();
}
const form = ref({
  name: "",
  phone: "",
  date: "",
  time: ""
});


</script>

<template>
<nav class="navbar navbar-expand-lg bg-body-tertiary" id="top">
  <div class="container-fluid">
    <a class="navbar-brand" style="color: brown;">Coffee_Cafe</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
      <div class="navbar-nav">
        <a class="nav-link" href="#The Nest Cafe">The Nest Cafe</a>
        <a class="nav-link" href="#TEA FAC">TEA FAC</a>
        <a class="nav-link" href="#Ristr8to">Ristr8to</a>
        <a class="nav-link" href="#ROAST8RY LAB">ROAST8RY LAB</a>
        <a class="nav-link" href="#Roxpresso Coffee Craft">Roxpresso Coffee Craft</a>

      </div>
    </div>
  </div>
</nav>
<div class="row row-cols-1 row-cols-md-2 g-4 p-1">
  <div class="card mb-3 col " v-for="i  in coffeeList">
    <img :src="i.link" class="card-img-top rounded mx-auto d-block " alt="..." :id="i.name" width="700" height="400">
    <div class="card-body">
      <h5 class="card-title">{{ i.name }}</h5>
      <p class="card-text"><small class="text-body-secondary">ช่วงราคา : {{ i.rate }} <br> เวลา เปิด-ปิด : {{ i.open }}</small></p>
      <p class="card-text">{{ i.reviwe }}</p>
      <button type="button" class="btn btn-warning" data-bs-toggle="modal" data-bs-target="#pageform" @click="ntable(i.name)" 
      .:value="i.name">จองโต๊ะน้า~~</button>
    </div>


    <div class="modal fade" id="pageform" data-bs-backdrop="static" data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticBackdropLabel" aria-hidden="true">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="staticBackdropLabel" v-for="i in list">{{ i.shop }}</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
          </div>
          <form class="modal-body form-box">
            <label for="namecos" class="form-label">ชื่อผู้จอง</label>
            <input type="text" id="namecos" class="form-control " v-model="form.name" placeholder="ชื่อ-นามสกุล"  required>
            <label for="tel" class="form-label">เบอร์โทรศัพท์</label>
            <input type="tel" id="tel" class="form-control" v-model="form.phone" placeholder="EX. 0865421586"  required>
            <label for="date" class="form-label">วันที่จอง</label>
            <input type="date" id="date" class="form-control" v-model="form.date" required>
            <label for="time" class="form-label">เวลาที่จอง</label>
            <input type="time" id="time" class="form-control" v-model="form.time" required>
          </form>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
            <button type="submit" class="btn btn-primary" data-bs-target="#exampleModalToggle2" data-bs-toggle="modal">Understood</button>    
          </div>
        </div>
      </div>
    </div>

    <div class="modal fade" id="exampleModalToggle2" data-bs-backdrop="static" data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticBackdropLabel2" aria-hidden="true">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="staticBackdropLabel">ยืนยันการจอง</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
          </div>
          <div class="modal-body" v-for="i in list">
            <p><strong>ร้านที่จอง:</strong> {{i.shop}}</p>
            <p><strong>ชื่อ-นามสกุล:</strong> {{ form.name }}</p>
            <p><strong>เบอร์โทร:</strong> {{ form.phone }}</p>
            <p><strong>วันที่:</strong> {{ form.date }}</p>
            <p><strong>เวลา:</strong> {{ form.time }}</p>
          </div>
          <div class="modal-footer" v-for="i in list">
            <button type="button" class="btn btn-danger" data-bs-target="#pageform" data-bs-toggle="modal">แก้ไข</button>
            <button type="button" class="btn btn-primary" @click="pushlist(i.name)" data-bs-target="#exampleModalToggle3" data-bs-toggle="modal" >ยืนยันการจอง</button>    
          </div>
        </div>
      </div>
    </div>

    <div class="modal fade" id="exampleModalToggle3" data-bs-backdrop="static" data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticBackdropLabel2" aria-hidden="true">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="staticBackdropLabel">จองสำเร็จ</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
          </div>
          <div class="modal-body">
            <div>ขอให้เป็นวันที่ดี~~</div>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
            <button type="button" class="btn btn-primary" @click="re()">ยืนยันการจอง</button>    
          </div>
        </div>
      </div>
    </div>
  </div>
</div>











<a href="#top" class="btn btn-primary btn-sm flybt opacity-50"><i class="fa-regular fa-circle-up"></i></a>
</template>

<style scoped>
    .flybt {
        position: fixed;
        right: 0px;
        bottom: 0px;
        margin: 1rem;
    }
    .form-box{
    justify-content: center;
    align-items: start;
    padding: 5px;
    margin-left: 30%;
    margin-right: 30%;
}
</style>
