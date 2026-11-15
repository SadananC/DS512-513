# DS512-513
## Sleep Quality Dataset
การวิเคราะห์และลดระยะเวลา Screen Time ก่อนนอนเพื่อเพิ่มคุณภาพการนอนหลับ
# 1. บทนำ (Introduction)
ปัจจุบันพฤติกรรมการใช้เครื่องมือสื่อสารและอุปกรณ์อิเล็กทรอนิกส์ก่อนนอน (Screen Time Before Bed) เช่น สมาร์ทโฟน แท็บเล็ต และคอมพิวเตอร์ กลายเป็นหนึ่งในปัจจัยหลักที่รบกวนวงจรการนอนหลับธรรมชาติ (Circadian Rhythm) แสงสีฟ้า (Blue Light) จากหน้าจอส่งผลยับยั้งการหลั่งฮอร์โมนเมลาโทนิน (Melatonin) ซึ่งทำให้ระยะเวลาการเข้าสู่นอน (Sleep Onset Latency) นานขึ้น และส่งผลกระทบเชิงลบต่อคุณภาพการนอนหลับโดยรวม

โครงการนี้ศึกษาชุดข้อมูลพฤติกรรมการนอนและปัจจัยทางสุขภาพของกลุ่มประชากรตัวอย่างจำนวน 374 รายการ โดยมุ่งเน้นศึกษาความสัมพันธ์ระหว่างพฤติกรรมการใช้หน้าจอก่อนนอน (Screen Time Before Bed) ช่วงอายุ (Age Groups) และคุณภาพการนอนหลับ (Quality of Sleep) เพื่อจัดทำแนวทางแก้ไขปัญหาเชิงพฤติกรรมอย่างตรงจุด
# 2. วัตถุประสงค์ (Smart Objectives)
เป้าหมายหลัก: ลดระยะเวลาการใช้หน้าจอก่อนนอนของกลุ่มคนวัยทำงานอย่างมีนัยสำคัญเพื่อยกระดับคะแนนคุณภาพการนอนหลับ
- S (Specific): ลดระยะเวลาการใช้หน้าจอก่อนนอน (Screen Time Before Bed) ของกลุ่มประชากรวัยทำงาน (อายุ 25-39 ปี) ซึ่งเป็นกลุ่มที่มี Screen Time สูงสุด
- M (Measurable): ลด Screen Time ก่อนนอนเฉลี่ยลงอย่างน้อย 20 นาที (จาก 73.85 นาที เหลือไม่เกิน 53.85 นาที หรือคิดเป็นลดลงประมาณ 27.1%) เพื่อเพิ่มคะแนนคุณภาพการนอนหลับเฉลี่ยจาก 7.06 เป็นไม่ต่ำกว่า 7.80/10 คะแนน
- A (Achievable): ปรับเปลี่ยนพฤติกรรมผ่านการกำหนดมาตรการ Digital Hygiene (เช่น การเปิด Do Not Disturb / Night Shift Mode และการงดใช้หน้าจอ 45 นาทีก่อนนอน)
- R (Relevant): มีความสัมพันธ์เชิงสถิติอย่างมีนัยสำคัญ โดย Screen Time มีความสัมพันธ์เชิงลบสูงกับคุณภาพการนอน ($r = -0.794, R^2 = 0.630$)
- T (Time-bound): บรรลุเป้าหมายภายในระยะเวลา 6 เดือนนับจากเริ่มดำเนินโครงการ
# 3. ตั้งคำถาม ระบุ Metric และ KPI  และรวบรวมข้อมูลที่เกี่ยวข้อง
3.1 คำถามวิจัย (Research Questions)
- RQ1: การใช้หน้าจอก่อนนอน (Screen Time Before Bed) มีความสัมพันธ์กับคุณภาพการนอนหลับ (Quality of Sleep) อย่างไร?
- RQ2: พฤติกรรมการใช้หน้าจอก่อนนอนและคุณภาพการนอนหลับ แตกต่างกันตามช่วงอายุหรือไม่?
- RQ3: หากสามารถลด Screen Time ก่อนนอนลงทุกๆ 15 นาที จะช่วยเพิ่มคะแนนคุณภาพการนอนหลับได้เท่าใด?

3.2 การกำหนด Metrics และ KPIs
- **Metric (ตัวแปร):** Screen Time Before Bed (mins) — ระยะเวลาการใช้หน้าจอก่อนนอน (KPI เป้าหมายที่แนะนำ: &le; 45 นาทีก่อนนอน)
- **KPIs (ตัวชี้วัดผลลัพธ์):**
  1. **Quality of Sleep:** คะแนนคุณภาพการนอนหลับเฉลี่ย (เป้าหมาย: &ge; 8)
  2. **Sleep Duration:** ระยะเวลาการนอนหลับเฉลี่ย (เป้าหมาย: &ge; 7.5 ชั่วโมง/คืน)
  3. **Sleep Disorder Prevalence (%):** สัดส่วนการเกิดโรค
     
# 4. แหล่งที่มาของข้อมูล (Data Source)
# 5. Data Dictionary

| Attribute | Description | Data Type | Valid Range / Example |
| :--- | :--- | :--- | :--- |
| Person ID | Person Identification Number | Ordinal | 1 - 347 |
| Gender | Gender of the person | Nominal | Male Female |
| Age | Age of the person | Ratio | 27 - 59 year |
| Occupation | Job of the person | Nominal | Accountant<br>Doctor<br>Engineer<br>Lawyer<br>Manager<br>Nurse<br>Sales Representative<br>Salesperson<br>Scientist<br>Software Engineer<br>Teacher |
| Sleep Duration | Number of hours the person sleeps (hours/day) | Ratio | 5.8 - 8.5 Hours |
| Quality of Sleep | Rating of sleep quality | Ordinal | 4 - 9 Level |
| Physical Activity Level | Physical activity (minutes/day) | Ratio | 30 - 90 Minute |
| Stress Level | Rating of stress level | Ordinal | 3 - 8 Level<br>1 - 3 ระดับต่ำ (Low Stress)<br>4 - 6 ระดับปานกลาง (Moderate Stress)<br>7 - 8 ระดับสูง (High Stress)<br>9 - 10 ระดับรุนแรงมาก (Severe / Extreme Stress) |
| BMI Category | The body Mass | Ratio | Normal OverweightObese |
| Blood Pressure | The blood pressure | Ratio | 115/75 - 142/92 |
| Heart Rate | The resting heart rate | Ratio | 65 - 86 bpm |
| Daily Steps | Number of steps (per day) | Ratio | 3000 - 10000 step |
| Sleep Disorder | Type of sleep | Nominal | None<br>Insomnia (ภาวะ โรคนอนไม่หลับ)<br>Sleep Apnea (ภาวะหยุดหายใจขณะหลับ) |

# 6. การวิเคราะห์ข้อมูลเชิงสำรวจ

# 7. Data Cleaning Process




# 8. Key Findings 
# 9. Action/Recommendation 

