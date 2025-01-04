<template>
  <div class="green-layout">
    <!-- Header -->
    <header class="layout-header">
      <h1 class="main-title">ผลลัพธ์และประสิทธิภาพ</h1>
    </header>


    <main class="layout-content">
      <div class="section-container">

        <div
          class="content-section"
          v-for="(section, index) in sections"
          :key="index"
        >
          <h3 class="section-title">{{ section.title }}</h3>
          <p>{{ section.content }}</p>
        </div>
      </div>
    </main>


  </div>
</template>

<script setup>
const sections = [
  {
    title: "การพัฒนาระบบที่อัตโนมัติและเพิ่มประสิทธิภาพการจัดตารางเวลา",
    content:
      "ระบบนี้ใช้เทคนิคการเรียนรู้ของเครื่องและอัลกอริธึมการเพิ่มประสิทธิภาพเพื่อทำให้กระบวนการจัดตารางเวลาเป็นไปอย่างอัตโนมัติและมีประสิทธิภาพ โดยระบบสามารถปรับปรุงและเรียนรู้จากข้อมูลที่ได้รับ เพื่อให้สามารถจัดการงานต่างๆ ได้อย่างเหมาะสมในสภาพแวดล้อมที่มีการเปลี่ยนแปลง​",
  },
  {
    title: "การเพิ่มประสิทธิภาพในการจัดการทรัพยากร",
    content:
      "ระบบนี้สามารถจัดสรรทรัพยากรได้อย่างมีประสิทธิภาพ โดยคำนึงถึงความพร้อมใช้งาน ทักษะ และความสามารถของทรัพยากรต่างๆ ซึ่งช่วยเพิ่มการใช้ทรัพยากรให้เกิดประโยชน์สูงสุดและหลีกเลี่ยงปัญหาความขัดแย้งของทรัพยากร​"
  },
  {
    title: "การเรียนรู้จากข้อมูลและการปรับตัวตามฟีดแบ็ก",
    content:
      "ระบบนี้จะเรียนรู้จากข้อมูลย้อนหลังและฟีดแบ็กจากผู้ใช้เพื่อลดข้อขัดแย้งในตารางเวลาและปรับการทำงานให้มีประสิทธิภาพยิ่งขึ้นตลอดเวลา​"
  },
];
</script>

<style scoped>
.green-layout {
  background-image: url('/assets/images/4.1.3.jpg');
  background-size: cover;
  background-position: center;
  background-color: rgba(0, 0, 0, 0.7);
  color: white;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  text-align: center;
}

.layout-header {
  background-color: rgba(0, 0, 0, 0.8);
  width: 80%;
  padding: 15px 0;
  border-radius: 50px;
  box-shadow: 0 0 20px rgba(211, 225, 8, 0.5), 0 0 15px rgba(0, 0, 0, 0.8);
}

.main-title {
  font-size: 2rem;
  font-weight: bold;
  background: linear-gradient(90deg, #ffba08, #ffec61);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
}

.layout-content {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content:  space-between; /* กึ่งกลางแนวนอน */
  width: 90%;
  max-width: 1000px;
  padding: 20px 0;
}

.section-container {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.content-section {
  background-color: rgba(0, 0, 0, 0.85);
  border: 2px solid #00ff80;
  border-radius: 16px;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 1.0);
  padding: 13px;
  text-align: left;
  font-size: 1.0rem;
}

.section-title {
  font-size: 1.2rem;
  font-weight: bold;
  color: #ffba08;
  margin-bottom: 10px;
}

.layout-footer {
  font-size: 0.85rem;
  color: #f1f1f1;
  text-align: center;
}
</style>
