<template>
  <div class="green-layout">
    <!-- Header -->
    <header class="layout-header">
      <h1 class="main-title">รายการบทความวิชาการ</h1>
    </header>

    <!-- Content -->
    <main class="layout-content">
      <div class="section-container">
        <!-- Section -->
        <div class="content-section" v-for="(article, index) in articles" :key="index">
          <h3 class="section-title">{{ article.title }}</h3>
          <p><strong>ประเภทบทความ:</strong> {{ article.type }}</p>
          <p><strong>ชื่อสิ่งตีพิมพ์:</strong> {{ article.publication }}</p>
          <p><strong>ปีที่ตีพิมพ์:</strong> {{ article.year }}</p>
          <p>
            <strong>ผู้เขียน:</strong>
            <span v-if="article.authors.length">{{ article.authors.join(', ') }}</span>
            <span v-else>ไม่มีการระบุชื่อผู้เขียน</span>
          </p>
        </div>
      </div>
    </main>


  </div>
</template>

<script setup>
const articles = [
  {
    title: "TIME LINE SCHEDULER USING AI",
    type: "Journal",
    publication: "Journal of Emerging Technologies and Innovative Research (JETIR)",
    year: "พฤษภาคม 2024",
    authors: ["M. Raju", "M. Arun Kumar", "J. Lokesh", "T. Ayusha", "Mrs. Uma"],
  },
  {
    title: "Intelligent Virtual Assistants with LLM-based Process Automation",
    type: "Proceedings",
    publication: "arXiv",
    year: "2023",
    authors: [
      "Yanchu Guan",
      "Dong Wang",
      "Zhixuan Chu",
      "Shiyu Wang",
      "Feiyue Ni",
      "Ruihua Song",
      "Longfei Li",
      "Jinjie Gu",
      "Chenyi Zhuang",
    ],
  },
  {
    title: "A Smart Personal AI Assistant for Visually Impaired People",
    type: "Journal",
    publication: "International Research Journal of Engineering and Technology (IRJET)",
    year: "2023",
    authors: [
      "Gagandeep Singh1",
      "Omkar Kandale",
      "Kevin Takhtani3",
      "Nandini Dadhwal"

    ],
  },
  {
    title: "An Intelligent Personal  Assistant for Task and  Time Management",
    type: "Journal",
    publication: "AI Magazine",
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
  title: "AutoDroid: LLM-powered Task Automation in Android",
  type: "proceeding",
  publication: "arXiv",
  year: "ธันวาคม 2023",
  authors: [
    "Hao Wen",
    "Yuanchun Li",
    "Guohong Liu",
    "Shanhui Zhao",
    "Tao Yu1,∗",
    "Toby Jia-Jun Li",
    "Shiqi Jiang",
    "Yunhao Liu",
    "Yaqin Zhang",
    "Yunxin Liu"
  ],


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
