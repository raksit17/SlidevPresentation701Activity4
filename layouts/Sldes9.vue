<template>
  <div class="green-layout">
    <!-- Header -->
    <header class="layout-header">
      <h1 class="main-title">วิธีการที่นำเสนอ</h1>
    </header>

    <!-- Content -->
    <main class="layout-content">
      <div class="section-container">
        <!-- Section -->
        <div class="content-section" v-for="(article, index) in articles" :key="index">
          <h3 class="section-title">{{ article.title }}</h3>
      
          <p>{{ article.publication }}</p>
   
        </div>
      </div>
    </main>


  </div>
</template>

<script setup>
const articles = [
  {
    title: "การวิเคราะห์ความต้องการ",
    publication: "มีส่วนร่วมกับผู้มีส่วนได้ส่วนเสียเพื่อรวบรวมข้อกำหนดรายละเอียดและทำความเข้าใจกับความต้องการในการจัดตารางเวลาของพวกเขา ขั้นตอนนี้จะทำให้มั่นใจว่าระบบการจัดตารางเวลาถูกออกแบบมาเพื่อตอบสนองความต้องการเฉพาะของผู้ใช้​",
  
  },
  {
    title: "การกำหนดวัตถุประสงค์",
    publication: "การกำหนดวัตถุประสงค์ของระบบจัดตารางเวลา เช่น การเพิ่มประสิทธิภาพในการจัดตารางงาน การปรับการใช้ทรัพยากร และการเพิ่มความพึงพอใจของผู้ใช้ ซึ่งช่วยในการตั้งเป้าหมายที่ชัดเจนสำหรับกระบวนการพัฒนา​",
  },
  {
    title: "การรวบรวมข้อมูลและการเตรียมข้อมูล",
    type: "Journal",
    publication: "การรวบรวมข้อมูลที่เกี่ยวข้อง เช่น ตารางเวลาที่ย้อนหลัง รายละเอียดงาน ความพร้อมของทรัพยากร และฟีดแบ็กจากผู้ใช้ ข้อมูลเหล่านี้จะเป็นพื้นฐานในการเรียนรู้และทำนายของอัลกอริธึม AI",
    year: "2023",
    authors: [],
  },
  {
    title: "Feature Engineering",
    type: "Journal",
    publication: "การระบุและสร้างคุณลักษณะที่เกี่ยวข้อง เช่น ระยะเวลาของงาน ลำดับความสำคัญ ความสัมพันธ์ระหว่างงาน และลักษณะของทรัพยากร คุณลักษณะเหล่านี้จำเป็นสำหรับ AI ในการเข้าใจและเพิ่มประสิทธิภาพของการจัดตารางงาน​",
    year: "ฤดูร้อน 2007",
    authors: [
      "Karen Myers",
      "Pauline Berry",
      "Jim Blythe",
      "Ken Conley",
      "Melinda Gervasio",
      "Deborah McGuinness",
      "David Morley",
      "Avi Pfeffer",
      "Martha Pollack",
      "Milind Tambe",
    ],
  },
  {
    title: "Machine Learning Algorithms",
    publication: "การใช้เทคนิคการเรียนรู้ของเครื่องขั้นสูงในการวิเคราะห์ข้อมูลงานย้อนหลัง รูปแบบการทำงานของแต่ละบุคคล และความสัมพันธ์ของโครงการ เพื่อให้ AI สามารถสร้างตารางเวลาที่เหมาะสมโดยให้ความสำคัญกับการกำหนดเวลา ความพร้อมของทรัพยากร และความสามารถของทีม​",

  },
  {
    title: "การเรียนรู้และการปรับตัวอย่างต่อเนื่อง",
    publication: "การสร้างระบบที่สามารถเรียนรู้และปรับตัวจากฟีดแบ็กแบบเรียลไทม์ ซึ่งจะช่วยปรับปรุงการทำนายและคำแนะนำของระบบตามเวลาที่ผ่านมา ทำให้มั่นใจได้ว่าระบบยังคงมีประสิทธิภาพในสภาพแวดล้อมที่มีการเปลี่ยนแปลง​",

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
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  text-align: center;
}
.main-title {
  font-size: 2rem;
  font-weight: bold;
  background: linear-gradient(90deg, #ffba08, #ffec61);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);


}
.layout-header {
  background-color: rgba(0, 0, 0, 0.8);
  width: 80%;
  padding: 15px 0;
  border-radius: 50px;
  box-shadow: 0 0 20px rgba(238, 255, 0, 0.5), 0 0 15px rgba(0, 0, 0, 0.8);
}

.gradient-title {
  font-size: 1.5rem;
  font-weight: bold;
  background: linear-gradient(90deg, #ffba08, #ffec61);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
  margin: 0;
}

.layout-content {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
  padding: 20px 0;
  font-size: 1rem; /* ปรับขนาดตัวอักษรสำหรับเนื้อหาทั้งหมด */
  line-height: 1.5; /* เพิ่มระยะห่างระหว่างบรรทัด */
}

.section-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 10px;
  width: 90%;
  max-width: 1000px;
}

.content-section {
  background-color: rgba(0, 0, 0, 0.85);
  border: 2px solid #00ff80;
  border-radius: 15px;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.5);
  padding: 6px;
  text-align: left;
  display: flex;
  flex-direction: column;
  font-size: 0.85rem; /* ลดขนาดตัวอักษรภายในกล่อง */
}

.section-title {
  font-size: 1.0rem;
  font-weight: bold;
  margin-bottom: 3px;
  color: #eae213; /* เปลี่ยนสีข้อความเป็นสีเหลือง */
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5); /* เพิ่มเงาให้ตัวอักษร */
  font-weight: bold; /* เน้นความหนา */
}
.content-section p strong {
  color: #ffba08; /* เปลี่ยนสีข้อความเป็นสีเหลือง */
  font-size: 0.9rem; /* ปรับขนาดตัวอักษร */
 
}

</style>
