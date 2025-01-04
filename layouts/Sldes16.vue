<template>
  <div class="green-layout">
    <!-- Header -->
    <header class="layout-header">
      <h1 class="main-title">งานวิจัยที่เกี่ยวข้อง</h1>
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
    title: "General Intelligence in AI",
    content:
      "เป้าหมายของปัญญาประดิษฐ์คือการพัฒนาเอเจนต์ที่สามารถทำงานเชิงปัญญาได้เหมือนมนุษย์ ",
  },
  {
    title: "Advancements in Intelligent Virtual Assistants",
    content:
      "ระบบเหล่านี้ช่วยให้งานประจำวันเป็นอัตโนมัติ แต่ยังมีข้อจำกัดในการจัดการคำสั่งหลายขั้นตอน​",
  },
  {
    title: "Integration of LLMs and Autonomous Agents",
    content:
      "การรวม LLMs กับเอเจนต์อัตโนมัติช่วยเพิ่มศักยภาพในการเข้าใจภาษาธรรมชาติและดำเนินการคำสั่งที่ซับซ้อน",
  },
  {
    title: "Instruction Chains",
    content:
      "เทคโนโลยีนี้ช่วยให้โมเดลสามารถแยกคำสั่งซับซ้อนออกเป็นขั้นตอนย่อยที่ชัดเจน",
  },
];
</script>

การจัดกลุ่มบทความตามเกณฑ์
บทความที่อัปโหลดมาสามารถจัดกลุ่มได้ตามเกณฑ์ดังนี้:

การพัฒนาเครื่องมือผู้ช่วยเสมือนอัจฉริยะด้วย LLM:

บทความ: Intelligent Virtual Assistants with LLM-based Process Automation​
, AutoDroid: LLM-powered Task Automation in Android​
.
เนื้อหา: การใช้โมเดลภาษาใหญ่ (LLM) เพื่อพัฒนาผู้ช่วยเสมือนที่สามารถดำเนินงานที่ซับซ้อนได้ เช่น การใช้งานแอปพลิเคชันมือถือ การจัดการ UI และการดำเนินการตามคำสั่งผู้ใช้.
การจัดการงานและการบริหารเวลา:

บทความ: TIME LINE SCHEDULER USING AI​
.
เนื้อหา: การพัฒนาระบบจัดการงานและตารางเวลาโดยใช้ AI และการเพิ่มประสิทธิภาพ.
การประยุกต์ใช้ AI ในการจัดการส่วนตัว:

บทความ: A Smart Personal AI Assistant​
, An Intelligent Personal Assistant for Task and Time Management​
.
เนื้อหา: ผู้ช่วยส่วนตัวที่ออกแบบมาเพื่อช่วยจัดการงานในชีวิตประจำวัน เช่น การกำหนดเวลา และการปรับตัวตามความต้องการผู้ใช้.