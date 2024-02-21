# ProjectSimpleJs1
First Project of Client side II
member
<ul>
<li>65130500017 ญาดา เจนรุ่งโรจน์สกุล</li>
<li>65130500021 ณัฐวรรณ คุ้มเผ่า</li>
<li>65130500029 ธิติพงศ์ สุดสวนศรี</li>
<li>65130500033 นภทีป์ จันทร์อินทร์ </li>
<li>65130500048 พสิษธ์ อุดมพานิช</li>
</ul>

# สรุปการประชุมงานวันจันทร์ที่ 28 ม.ค.
หลังจากการประชุมเราสรุปได้ว่า จากprototypeแรกที่ได้ลองทำมานั้นได้มีการ update idea ของตนเอง และ ได้แลกเปลี่ยนlogicที่ได้ไปทำมา เราได้มีการปรับเปลี่ยน และสิ่งที่เพิ่มมาดังนี้ 
* มี Tutorial สำหรับสอนเล่นซึ่งจะเป็น pop up เด้งขึ้นมา
* มีโหมดสำหรับจับเวลาการเล่น
* มีโหมดสำหรับการจำกัดเวลาการเล่น
* มีปุ่มHint สำหรับกดเพื่อ fiil ในช่องที่ถูกต้อง

เราได้มอบหมายงานให้ทุกคนทำmini project ในรูปแบบของตนเอง เพื่อที่จะเลือกแต่ละfunction ที่ดีที่สุดจากทุกproject แล้วจึงนำมาmerge รวมเป็น main project

  # ProjectSimpleJs1
First Project of Client side II
member
<ul>
<li>65130500017 ญาดา เจนรุ่งโรจน์สกุล</li>
<li>65130500021 ณัฐวรรณ คุ้มเผ่า</li>
<li>65130500029 ธิติพงศ์ สุดสวนศรี</li>
<li>65130500033 นภทีป์ จันทร์อินทร์ </li>
<li>65130500048 พสิษธ์ อุดมพานิช</li>
</ul>

Week 1 Progress:
- [x] Proof of Concept
- [x] Basic UX-UI design
- [x] Base game concept

Week 2 Progress:
- [x] Basic UX-UI Implementation
- [x] Adapting codebase to use Vue directives

Week 3 Progress:
- [x] Hinting System
- [x] Timer
- [x] Tutorial Modal
- [x] Changing Level mechanic

Next steps:
- [x] Implementing Main Menu
- [x] Full UX-UI CSS 
- [x] Saving system using local storage


# Features list
### 1.Tutorials 
* multiple pages tutorial สามารถกดเปลี่ยนหน้า tutorial ได้
* มีปุ่มเปลี่ยนหมวดหมู่ของ tutorial สองปุ่ม: General, Game Modes

### 2.Game Play
#### Easy mode และ Hard mode
* เมื่อกดเริ่มเกม ระบบจะสุ่มเลือก object ด่านจาก level JSON file มา 5 level จาก level ทั้งหมดใน file แล้วนำค่ามาใส่ใน template เกม
* ผู้เล่นสามารถคลิกซ้ายในการเลือกช่อง (check) โดยจะแสดงเป็นสีเขียวถ้าเป็นblockที่ถูกและ สีแดงถ้าเป็นblockที่ผิดแล้วไปเพิ่มค่า missed
* ผู้เล่นสามารถกดคลิกขวาในกรณีที่ต้องการกด mark ไม่ให้กดคลิกซ้ายได้เป็นการกันช่อง คล้ายกับการตัด choice และสามารถกดคลิกขวาอีกครั้งเพื่อนำmarkออก
* มี Hint เป็นตัวช่วย(Easy mode 3 ครั้ง และHard mode 5 ครั้ง)ในแต่ละlevel โดยเมื่อผู้เล่นกดปุ่มHint 1 ครั้ง จะ ทำการrandom block ที่ถูก และเฉลยเป็นสีเขียวในblockนั้นให้ ในกรณีที่ผู้เล่นได้ mark ช่องที่ถูกต้องและเหลือเป็น block สุดท้ายปุ่ม mark จะไม่ถูก disable แสดงถึงยังมี block ที่ยังไม่ถูกกด เมื่อเล่นจบด่านนั่นคือ block ที่ถูกถูก check จนครบปุ่มนี้ก็จะถูกปิดไป
* มีเวลานับตั้งแต่เริ่มเล่นจนเล่นครบทั้ง 5 level
* มี Best time ที่เป็นเวลาที่ดีที่สุดของผู้เล่นเก็บไว้ในlocal storage ถ้าผู้เล่นเล่นในEasy mode จะถูกเก็บไว้ใน Localstorage item ชื่อ “easyMode” ถ้าผู้เล่นเล่นในHard mode จะถูกเก็บไว้ใน Localstorage item ชื่อ “hardMode” และแสดงในทุก level ที่เล่นขึ้นอยู่กับ mode ที่เล่น
* มีค่าMissในการระบุว่ากดblockที่ผิดไปกี่ครั้งแล้วตั้งแต่เริ่มเล่น โดยถ้าค่าMiss ของEasy levelเกิน5 ครั้ง และHard levelเกิน10ครั้งจะเข้าสู่ modal แพ้เกม

### 3.Modal Page
* เมื่อผู้เล่น เล่นครบทั้ง 5 level หน้า modal page จะแสดงขึ้นมา เพื่อระบุBest time และ เวลาที่ใช้ทั้งหมดในการเล่น โดยจะมีข้อความแตกต่างกันไปในแต่ละกรณีเช่น หากเวลาเล่นเร็วกว่า Best time จะแสดงความยินดีต่อผู้เล่น หรือ หากช้ากว่าหรือเท่ากับ best time จะมีข้อความบอกให้ผู้เล่นเพิ่มความเร็ว

# Instruction Manual
Number Hunter เป็นเกมปริศนาเชิงตรรกะ ที่ให้ผู้เล่นทดสอบทักษะของตนด้วยการไขปริศนาที่เกี่ยวข้องกับการเติมเซลล์บนตารางตามคำใบ้ที่บอกด้วยตัวเลขสำหรับแต่ละแถวและคอลลัมน์เพื่อให้ได้รูปภาพที่เกมกำหนด
### ขั้นตอนการเริ่ม
เมื่อผู้เล่นอยู่ที่หน้าแรก จะสามารถเลือกการเข้าถึงเกมในโหมดง่าย(easy mode) โหมดยาก(hard mode) หรือเกี่ยวกับการสอน(tutorial)ได้
### tutorial
เมื่อเข้ามาที่หน้าเกี่ยวกับการสอน ผู้เล่นจะพบกับการสอนพื้นฐานที่จะแนะนำวิธีการเล่นและหลักการทั่วไปของเกม และการแนะนำตามโหมด ด้วยการกดปุ่มGame mode ผู้เล่นสามารถกลับไปดูการสอนพื้นฐานได้อีกครั้งด้วยการกดปุ่ม general 
### ระดับความยาก
ผู้เล่นสามารถเลือกระดับความยากได้ที่หน้าแรก โดยจะมีให้เลือก2โหมด คือโหมดง่าย(easy mode)และโหมดยาก(hard mode) ในแต่ละโหมดผู้เล่นจะต้องผ่านด่านทั้งหมด5ครั้งถึงจะจบเกม
### How to play
- ในแต่ละแถวและคอลลัมน์จะมีตัวเลขกำหนดไว้ ซึ่งตัวจะเป็นตัวกำหนดว่าผู้เล่นจะต้องเติมเซลล์ในตารางเป็นจำนวนเท่าไหร่
- เมื่อมีตัวเลขหลายตัวถัดจากแถวหรือคอลลัมน์ ตัวเลขเหล่านั้นแสดงถึงกลุ่มของช่องที่มีจำนวนต่างกัน สิ่งสำคัญคือต้องมีช่องว่างอย่างน้อยหนึ่งช่องระหว่างกลุ่มเหล่านี้
- วิธีการเติมเซลล์ในตาราง ให้ผู้เล่นทำการคลิกซ้ายไปที่ช่องที่ต้องการ ถ้าเป็นช่องที่ถูกต้องเซลล์จะกลายเป็นสีเขียว แต่เมื่อเป็นช่องที่ผิด เซลล์จะกลายเป็นสีแดง นอกจากนี้ผู้เล่นยังสามารถบล็อกเซลล์ที่คิดว่าไม่ใช่ด้วยการคลิกขวาไปยังช่องที่ต้องการเพื่อ... และสามารถยกเลิกการบล็อกนั้นด้วยการคลิกขวาซ้ำในช่องเดิม
- ในแต่ละด่านผู้เล่นสามารถกดปุ่ม hint เพื่อรับคำใบ้เพิ่มจากเกม โดยเป็นการเติมเซลล์ในช่อง ในโหมดง่ายเป็นจำนวน 3 ครั้งและในโหมดยากเป็นจำนวน 5 ครั้ง
- ในแต่ละโหมดจะมีกำหนดจำนวนครั้งที่ผิดพลาด โดยในโหมดง่ายเป็นจำนวนไม่เกิน 5 ครั้งและในโหมดยากเป็นจำนวนไม่เกิน 10 ครั้ง เมื่อผู้เล่นพลาดเกินที่เกมกำหนด จะต้องเริ่มต้นเกมใหม่ทั้งหมด
- ทุกโหมด จะมีการท้าทายเวลาผู้เล่นด้วยการจับเวลาการเล่นตั้งแต่ด่านที่1ถึงด่านที่5 จนจบเกม


## คลิปสาธิต features


## แหล่งอ้างอิง

### 4.Fail page
* เมื่อค่าMiss ของEasy levelเกิน5 ครั้ง และHard levelเกิน10ครั้ง Fail page จะแสดงขึ้นมา ให้เลือกเริ่มเล่นอีกครั้ง หรือกลับไปหน้าHome


