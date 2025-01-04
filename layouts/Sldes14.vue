<template>
  <div class="green-layout">
    <!-- Header -->
    <header class="layout-header">
      <h1 class="main-title">ผลกระทบของปัญหา</h1>
    </header>

    <!-- Content -->
    <main class="layout-content">
      <div class="grid-container">
        <!-- Sections -->
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

    <!-- Footer -->
    <footer class="layout-footer">
      <p>© 2024 AI Scheduler Presentation</p>
    </footer>
  </div>
</template>

<script setup>
const sections = [
  {
    title: "การใช้งานผู้ช่วยเสมือนอย่างแพร่หลาย",
    content:
      "ผู้ช่วยเสมือน เช่น Siri, Alexa และ Google Assistant กลายเป็นส่วนสำคัญในชีวิตประจำวัน แต่ยังมีข้อจำกัดในการดำเนินการคำสั่งที่ซับซ้อนหลายขั้นตอน หากสามารถปรับปรุงความสามารถในด้านนี้ได้ จะช่วยเพิ่มประสิทธิภาพและประสบการณ์ผู้ใช้ให้ดีขึ้นสำหรับผู้คนนับล้านทั่วโลก",
  },
  {
    title: "การประยุกต์ใช้ในโลกจริงและการใช้งานในวงกว้าง",
    content:
      "งานวิจัยนี้แสดงถึงการนำระบบผู้ช่วยเสมือนที่ขับเคลื่อนด้วยโมเดลภาษาใหญ่ (LLM) มาใช้จริงในแอป Alipay ซึ่งมีผู้ใช้งานนับร้อยล้านคน ความสามารถในการจัดการคำสั่งซับซ้อนในสถานการณ์จริงแสดงถึงศักยภาพที่จะเปลี่ยนแปลงวิธีการใช้งานเทคโนโลยีในระดับใหญ่",
  },
  {
    title: "ความก้าวหน้าใน AI และระบบอัตโนมัติ",
    content:
      "การพัฒนาโมเดล LLM ทำให้ผู้ช่วยเสมือนสามารถเข้าใจคำสั่งเชิงซับซ้อนและทำงานที่ซับซ้อนโดยอัตโนมัติ ",
  },
  {
    title: "การแก้ปัญหาความซับซ้อนของงานในโลกดิจิทัล:",
    content:
      "ผู้ช่วยเสมือนที่สามารถจัดการคำสั่งซับซ้อนได้ จะช่วยลดภาระของผู้ใช้ในการทำงานที่ยุ่งยาก",
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
  justify-content: center;
  align-items: center;
  width: 90%;
  max-width: 1200px;
  padding: 20px 0;
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  width: 100%;
}

.content-section {
  background-color: rgba(0, 0, 0, 0.85);
  border: 2px solid #00ff80;
  border-radius: 15px;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.5);
  padding: 20px;
  text-align: left;
  font-size: 0.9rem;
}

.section-title {
  font-size: 1.2rem;
  font-weight: bold;
  color: #cdc845;
  margin-bottom: 10px;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
}

.layout-footer {
  font-size: 0.85rem;
  color: #f1f1f1;
  text-align: center;
}
</style>