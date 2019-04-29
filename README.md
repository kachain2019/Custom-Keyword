# How to Custom Keyword ?

```
# Main Cross คือการ Copyของคนอื่นมา อ่านให่ได้ แก้ให้เป็น = Custom Keyword

# เราจะมาพูดถึงเรื่องของการ Custom Keyword ครับ
  - git clone https://github.com/kachain2019/Custom-Keyword.git

# Generate keyword document
$python -m robot.libdoc HelloLibrary HelloLibrary.html
เป็นคำสั่งในการสร้าง Document ไฟล์ที่มีชื่อว่า HelloLibrary.html รันคำสั่งแล้วลองเปิดไฟล์ดูนะครับ
ถ้าเราเขียนถูกมันจะมีคำอธิบายการใช้ Library ที่เราสร้างใน Document ด้วยครับ

# Run file use._csv.robot
$robot --pythonpath . use_csv.robot

# อธิบายคร่าวๆครับ
  - เปิด https://github.com/s4int/robotframework-CSVLibrary/blob/master/CSVLibrary/__init__.py 
    ลิ้งข้างบนคือตัวอย่างที่มีคนอื่นได้ทำเอาไว้ครับ เราสามารถเข้าไปศึกษาและมา Custom เป็นของเราเองได้ เพราะเราไม่สามารถอ่านโค้ดของเขาออกแน่นอน 
    ดังนั้น เราจะมาดูในจุดที่เราสนใจคือการทำให้อา่นไฟล์ csv ได้เท่านั้น
  - เราสร้างไฟล์ที่ชื่อ __init__.py มันคือไฟล์ที่ Autorun ให้นะครับ คือไม่ต้องระบุ path ไฟล์ในการรัน คือเราเรียกแค่ชื่อโฟลเดอร์ก็พอ ไม่ต้องระบุชื่อไฟล์
  - ดูในไฟล์ __init__.py จะเห็นว่ามีโค้ดไม่กี่บรรทัดก็สามารถอ่านไฟล์ csv ได้แล้ว เจ๋งไหมครับ
    >> บรรทัดที่ 1  คือการ import csv 
    >> บรรทัดที่ 2  def read_file_to_list(filename): การสร้างฟังก์ชั่นที่ชื่อว่า read_file_to_list ที่มี Argument 1ตัวคือ (filename)
    >> บรรทัดที่ 3  users = csv.reader(csvfile) ให้เราดูที่ .reader ครับ มันคือฟงก์ชั่นของ Python ที่สั่งให้อ่านไฟล์ เก็บข้อมูลที่ได้ในตัวแปร user
    >> บรรทัดที่ 4  next(users, None) ไม่เอาหัวตารางของไฟล์ครับ
    >> บรรทัดที่ 5  return [rows for rows in users] ส่งค่ากลับไปตามตัวแปร users
    จะเห็นว่าการอ่านไฟล์ csv จริงๆแล้วใช้โค้ดไม่กี่บรรทัดก็สามารถใช้งานได้เหมือนกันแล้วครับ จริงๆความรู้ในอินเตอร์เน็ตมันเปิดกว้างมากเลยครับ ถ้าเราทำเองยังไม่ได้ ให้ศึกษาจาการอ่านของคนที่ทำๆด้ให้เข้าใจแล้วมาลงมือทำครับ
```

# How to Up Library ?

```
* ต่อมาผมจะมาสอนการอัพไฟล์ HelloLibrary.py ให้ชาวโลกได้ใช้งานกันครับ สอนเพียงขั้นตอนการอัพนะครับ เพื่อเป็นแนวทางเผื่อว่าใครที่ได้เขียน Library ใช้กันเองในองค์กรหรือเฉพาะทาง จะได้รู้ขั้นตอนในการทำครับ



# Custom-Keyword
