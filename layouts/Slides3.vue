<template>
  <div class="green-layout">
    <br>
    <header class="layout-header">
      <h1 class="gradient-title">{{ frontmatter.title }}</h1>
    </header>
    <main class="layout-content">
      <div class="content-row">
        <!-- Box 1 -->
        <div class="content-box">
          <slot name="box1" />
        </div>
        <!-- Box 2 -->
      </div>
    </main>
    <footer class="layout-footer">
      <!-- Footer -->
    </footer>
  </div>
</template>

<script setup>
defineProps(['frontmatter']); // รับค่า Front Matter
</script>

<style scoped>
.green-layout {
  background-image: url('/assets/images/4.1.3.jpg'); /* พื้นหลัง */
  background-size: cover;
  background-position: center;
  background-color: rgba(0, 0, 0, 0.7); /* เพิ่ม overlay */
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
  background-color: rgba(0, 0, 0, 0.8); /* โปร่งแสง */
  width: 80%;
  padding: 15px 0;
  border-radius: 50px; /* เพิ่มมุมโค้ง */
  box-shadow: 0 0 20px rgba(0, 255, 128, 0.5), /* เงาสีเขียว */
              0 0 15px rgba(0, 0, 0, 0.8); /* เงาสีดำ */
}


.gradient-title {
  font-size: 2.0rem;
  font-weight: bold;
  background: linear-gradient(90deg, #ffba08, #ffec61);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5); /* เพิ่มเงาสำหรับความชัดเจน */
  margin: 0;
}

.layout-content {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center; /* จัดตรงกลาง */
  align-items: center;
  width: 100%;
  padding: 20px 0;
}

.content-row {
  display: flex; /* ใช้ Flexbox */
  flex-wrap: wrap; /* รองรับหน้าจอเล็ก */
  justify-content: space-between; /* กล่องอยู่ซ้ายขวา */
  gap: 20px; /* ระยะห่างระหว่างกล่อง */
  width: 90%; /* กำหนดความกว้างรวม */
  max-width: 1200px; /* จำกัดความกว้างสูงสุด */
}

.content-box {
  background-color: rgba(0, 0, 0, 0.85); /* สีพื้นหลังเข้มขึ้น */
  border: 2px solid #00ff80; /* เปลี่ยนสีกรอบเป็นสีเขียวสว่าง */
  padding: 30px; /* เพิ่มระยะห่างภายใน */
  border-radius: 15px; /* เพิ่มขอบมนให้ดูนุ่มนวล */
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.5); /* เพิ่มเงาเพื่อความลึก */
  max-width: 800px;
  color: #e5ffe5; /* เปลี่ยนสีข้อความเป็นสีเขียวอ่อน */
  font-size: 1.2rem; /* ขนาดข้อความ */
  line-height: 1.8; /* ระยะห่างระหว่างบรรทัด */
  text-align: left; /* ชิดซ้าย */
  width: 90%; /* ขยายความกว้าง */
  margin: 20px auto; /* จัดกึ่งกลาง */
  display: flex;
  flex-direction: column;
  align-items: flex-start; /* จัดชิดซ้าย */
}

.sub-title {
  font-size: 1.5rem;
  font-weight: bold;
  background: linear-gradient(45deg, #71ff64, #1ed758); /* สีข้อความ */
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.7); /* เพิ่มเงาสำหรับความชัดเจน */
  margin: 10px 0;
}
</style>
