# Data Structures in C 
- **Data Structures** คือ วิธีการจัดเก็บและจัดการข้อมูลในคอมพิวเตอร์เพื่อให้สามารถเข้าถึงและแก้ไขข้อมูลได้อย่างมีประสิทธิภาพ ตัวอย่างของโครงสร้างข้อมูล ได้แก่ อาร์เรย์, ลิงก์ลิสต์, สแตก, คิว, และต้นไม้

### Array และ Linked List: 
- เป็น โครงสร้างข้อมูลพื้นฐาน (basic data structures) ที่ใช้ในการจัดเก็บข้อมูล เป็นลำดับ (sequential). Array ใช้การจัดเก็บข้อมูลในหน่วยความจำที่ต่อเนื่อง, ขณะที่ Linked List ใช้ โหนด (nodes) ที่เชื่อมโยงกันผ่าน ตัวชี้ (pointers).

### Stack, Queue, Tree, และ Graph: เป็น โครงสร้างข้อมูลขั้นสูง (advanced data structures) ที่ถูกสร้างขึ้นจากการใช้ Array หรือ Linked List:
- Stack: สร้างขึ้นจาก Array หรือ Linked List โดยใช้หลักการ LIFO (Last In, First Out).
- Queue: ใช้หลักการ FIFO (First In, First Out).
- Tree: เป็นโครงสร้างแบบลำดับชั้น (hierarchical) ที่ใช้โหนดและตัวชี้ในการสร้างความสัมพันธ์ระหว่างข้อมูล.
- Graph: เป็นโครงสร้างที่ซับซ้อนกว่า โดยโหนดจะเชื่อมกันด้วยเส้นเชื่อม (edges) ซึ่งอาจสร้างจาก Array หรือ Linked List.

### สรุปง่ายๆ:
- Array และ Linked List เป็นโครงสร้างพื้นฐาน.
- Stack, Queue, Tree, และ Graph เป็นโครงสร้างที่ซับซ้อนกว่า ซึ่งสามารถสร้างขึ้นจาก Array หรือ Linked List.

## Array 
- **Array** เป็นโครงสร้างข้อมูลพื้นฐานในภาษา C ที่ใช้ในการจัดเก็บชุดของข้อมูลประเภทเดียวกันในตำแหน่งที่ต่อเนื่องกันในหน่วยความจำ โดยการเข้าถึงข้อมูลในอาเรย์สามารถทำได้โดยใช้ดัชนี (index)

<img width="1000" alt="Array1" src="https://github.com/user-attachments/assets/21e2ec50-7ebc-4384-8e31-9910f5834381">  

### การประกาศ Array 
>  ***data_type array_name[array_size];***
- **data_type:** ชนิดข้อมูลของสมาชิกในอาร์เรย์ (เช่น int, float, char เป็นต้น)
- **array_name:** ชื่อของอาร์เรย์
- **array_size:** ขนาดของอาร์เรย์ (จำนวนสมาชิกที่ต้องการเก็บ)
- เช่น **int numbers[5];**

### 2 Dimensional Array 
<img width="1000" alt="Array1" src="https://github.com/user-attachments/assets/a0462539-d61f-4cb3-995e-d9c33f178b3a">  

### การใช้งาน Array 
- **การเข้าถึงสมาชิก:** สามารถใช้ดัชนี (index) เพื่อเข้าถึงสมาชิกในอาร์เรย์ เช่น array[index]
- **การกำหนดค่า:** สามารถกำหนดค่าให้กับสมาชิกได้โดยการใช้ดัชนี เช่น array[index] = value
- **การวนลูป:** สามารถใช้ลูปเพื่อทำงานกับสมาชิกทั้งหมดของอาร์เรย์ เช่น การแสดงผลทุกสมาชิกในอาร์เรย์
  
## Node 
- **Node** เป็นหน่วยพื้นฐานที่ใช้ในการจัดเก็บข้อมูลและเชื่อมโยงไปยังโหนดอื่นๆ 

<img width="1000" alt="Node" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRJ5F4EBEjzdiJ5sNTIuvsjiz1lCJVj2Q-vMA&s">  

### Node แต่ละตัวมีสองส่วนหลัก
- **Data (ข้อมูล):** ใช้ในการจัดเก็บข้อมูลที่เราต้องการ เช่น ตัวเลข ข้อความ หรือข้อมูลประเภทอื่น
- **Pointer (ตัวชี้):** ใช้ในการเชื่อมโยงโหนดปัจจุบันไปยังโหนดถัดไปในลิสต์ (หรือโหนดก่อนหน้าในกรณีของลิงก์ลิสต์แบบสองทิศทาง)
  
### การใช้งานของ Node 
- โหนดเป็นหน่วยที่เชื่อมต่อกันในลิงก์ลิสต์โดยการอ้างอิงถึงกัน ทำให้สามารถสร้างลิสต์ที่มีขนาดแตกต่างกันตามความต้องการของโปรแกรม

## Linked List
- **Linked List** คือโครงสร้างข้อมูลเชิงเส้นที่ใช้ในการจัดเก็บชุดของข้อมูลซึ่งองค์ประกอบแต่ละตัวจะเชื่อมต่อกันโดยการอ้างอิง (pointer) ในแต่ละองค์ประกอบของลิงก์ลิสต์จะมีสองส่วนหลัก คือ ข้อมูล (data) และตัวชี้ (pointer) ที่เชื่อมโยงไปยังองค์ประกอบถัดไปในลิสต์

<img width="1000" alt="linklist" src="https://media.geeksforgeeks.org/wp-content/uploads/20220712172013/Singlelinkedlist.png">

- **Next:** ใช้ในการเชื่อมต่อ node แต่ละตัวใน Linked List เข้าด้วยกัน
- **Head/Start:** เป็นจุดเริ่มต้นของ Linked List และใช้ในการเข้าถึง node ตัวแรก

### 1. Singly Linked List
- Singly Linked List เป็น Linked List พื้นฐานที่สุด แต่ละโหนดมีพอยน์เตอร์ที่ชี้ไปยังโหนดถัดไปเท่านั้น

<img width="1000" alt="Screenshot 2567-07-25 at 13 52 57" src="https://github.com/user-attachments/assets/ac79e284-104e-471e-8a7c-7afd6e497419">

### 2. Doubly Linked List
- Doubly Linked List แต่ละโหนดมีสองพอยน์เตอร์ ชี้ไปยังโหนดก่อนหน้าและโหนดถัดไป ทำให้สามารถเดินทางทั้งไปข้างหน้าและย้อนกลับได้

<img width="1000" alt="Screenshot 2567-07-25 at 13 53 13" src="https://github.com/user-attachments/assets/697abcbf-759a-495a-a744-d27d9fc13df7">

### 3. Circular Linked List
- Circular Linked List เป็น Singly Linked List ที่โหนดสุดท้ายชี้กลับไปที่โหนดแรก ทำให้โครงสร้างเชื่อมต่อเป็นวงกลม

<img width="1000" alt="Screenshot 2567-07-25 at 13 53 39" src="https://github.com/user-attachments/assets/2faef863-39ed-4073-a348-f4a0c52fe68a">

### 4. Circular Doubly Linked List
- Circular Doubly Linked List เป็น Doubly Linked List ที่โหนดสุดท้ายชี้กลับไปยังโหนดแรกและโหนดแรกชี้ไปยังโหนดสุดท้าย ทำให้เชื่อมต่อเป็นวงกลมทั้งไปข้างหน้าและย้อนกลับ

<img width="1000" alt="Screenshot 2567-07-25 at 13 53 49" src="https://github.com/user-attachments/assets/9f68db83-a718-4ded-a370-204554e9c3ef">

### กรณีการใช้งาน Linked List
 1. **จัดการหน่วยความจำที่ไม่ต่อเนื่อง:** ใช้เมื่อขนาดของข้อมูลไม่แน่นอน เช่น การจัดการรายการในโปรแกรมที่ต้องการเพิ่มหรือลบข้อมูลบ่อยๆ
 2. **แทรกและลบข้อมูลอย่างมีประสิทธิภาพ:** เพิ่มหรือลบข้อมูลง่ายกว่าการใช้อาร์เรย์ โดยไม่ต้องเลื่อนข้อมูล
 3. **จัดเก็บข้อมูลที่ต้องการการเข้าถึงแบบลำดับ:** ใช้สำหรับรายการที่ต้องการการเข้าถึงข้อมูลแบบเป็นลำดับ เช่น รายการเพลง
 4. **สร้างโครงสร้างข้อมูลที่ซับซ้อน:** ใช้เป็นฐานในการสร้างโครงสร้างข้อมูลที่ซับซ้อน เช่น ต้นไม้หรือกราฟ
 5. **การเดินทางในทิศทางทั้งสอง:** ใช้ลิงก์ลิสต์แบบสองทิศทางเพื่อการเดินทางไปข้างหน้าและย้อนกลับ

## Stack
- **Stack** คือโครงสร้างข้อมูลเชิงเส้นที่ทำงานตามหลักการ Last In, First Out (LIFO) หมายความว่าองค์ประกอบที่ถูกเพิ่มเข้ามาเป็นองค์ประกอบสุดท้ายจะถูกนำออกเป็นองค์ประกอบแรก สามารถนึกภาพได้ว่าเหมือนกับกองจานที่เราสามารถเพิ่มหรือเอาจานออกจากด้านบนสุดเท่านั้น

<img width="600" alt="Stack1" src="https://github.com/user-attachments/assets/7824c5ec-c513-465b-8129-2a7cecc7eaa4"> 

### การดำเนินการหลักของ Stack
- **Push:** เพิ่มองค์ประกอบไปที่ด้านบนสุดของ stack
- **Pop:** นำองค์ประกอบออกจากด้านบนสุดของ stack
- **Peek:** ดูองค์ประกอบที่อยู่ด้านบนสุดของ stack โดยไม่ต้องนำออก
- **isEmpty:** ตรวจสอบว่า stack ว่างหรือไม่

<img width="1000"  alt="Stack2" src="https://github.com/user-attachments/assets/e851c382-a3a9-443d-adaf-0bdd3f963a5d">
  
### กรณีการใช้งาน Stack
- การจัดการการเรียกฟังก์ชัน (recursion)
- กลไกการย้อนกลับ (undo) ในโปรแกรมแก้ไขข้อความ
- การวิเคราะห์ไวยากรณ์ (เช่น การตรวจสอบการจับคู่ของวงเล็บ)
- อัลกอริทึม backtracking (เช่น การแก้ปัญหาเขาวงกต)

## Queue
- **Queue** คือโครงสร้างข้อมูลพื้นฐานที่ทำงานบนหลักการ "เข้าก่อนออกก่อน" FIFO(First-In-First-Out) หมายถึงข้อมูลที่ถูกเพิ่มเข้าไปในคิวก่อนจะถูกนำออกมาก่อน

<img width="1000"  alt="Queue1" src="https://github.com/user-attachments/assets/3a1865c3-f5df-4e3f-a46b-9cb0e52ce0c6"> 

### Front (Head):
- ตำแหน่งที่เก็บข้อมูลตัวแรกสุดในคิว
- ใช้สำหรับการนำข้อมูลออกจากคิว (dequeue)
- ข้อมูลที่ถูกเพิ่มเข้ามาก่อนจะถูกนำออกก่อน (หลักการ FIFO)

### Rear (Back/Tail):
- ตำแหน่งที่เก็บข้อมูลตัวสุดท้ายในคิว
- ใช้สำหรับการเพิ่มข้อมูลเข้าคิว (enqueue)
- ข้อมูลที่ถูกเพิ่มเข้ามาหลังสุดจะถูกนำออกหลังสุด

### การใช้งาน Queue
- **Enqueue/insert (เพิ่มข้อมูล):** เพิ่มข้อมูลใหม่ที่ปลายคิว
- **Dequeue/delete (นำข้อมูลออก):** นำข้อมูลจากหัวคิวออก
- **Display/peek:** แสดงข้อมูลทั้งหมดในคิว

<img width="600"  alt="Queue2" src="https://github.com/user-attachments/assets/a6bf85d8-2f0f-4713-8d0e-bc5edcc856e9">

### กรณีการใช้งาน Queue
- **การจัดการคิวของงาน:** ในระบบปฏิบัติการ การจัดการกับงานที่ต้องทำให้เสร็จตามลำดับ
- **การจัดการกับการพิมพ์:** ในระบบที่มีการพิมพ์เอกสารจากหลายแหล่ง ข้อมูลของเอกสารจะถูกจัดเก็บในคิว
- **การจัดการกับการสื่อสารข้อมูล:** การส่งข้อมูลผ่านเครือข่าย ที่ข้อมูลจะถูกจัดเก็บในคิวก่อนการส่งต่อไปยังปลายทาง
- **การจัดการเหตุการณ์ในเกม:** การจัดการกับเหตุการณ์ที่เกิดขึ้นในเกมตามลำดับ

## Trees

- **Trees** คือโครงสร้างข้อมูลชนิดหนึ่งที่เป็นแบบลำดับชั้น (hierarchical) 
โดยมีการเชื่อมโยงกันเป็นลำดับของโหนด (nodes) ซึ่งต้นไม้ (Tree) เป็นโครงสร้างข้อมูลที่ใช้อย่างแพร่หลายในการจัดการข้อมูลเชิงลำดับที่ซับซ้อน เช่น โครงสร้างแฟ้มข้อมูล โครงสร้างของเว็บไซต์ หรือการจัดการฐานข้อมูล.

### โครงสร้างข้อมูลแบบลำดับชั้น (Hierarchical Structure)
- โครงสร้างข้อมูลแบบลำดับชั้นจัดเก็บข้อมูลเป็นลำดับชั้น มีการเชื่อมโยงกันระหว่างโหนด (Node).
- โหนดมีโหนดราก (Root Node) เป็นโหนดเริ่มต้น และมีลูกโหนด (Child Nodes) เป็นโหนดย่อยที่เชื่อมต่อกันในรูปแบบต้นไม้.

![Treedatastructure](https://github.com/user-attachments/assets/23c5fa76-00fe-41b4-959b-72b3c52d6d46)
  
#### องค์ประกอบของ Trees:
- Root (ราก): โหนดเริ่มต้นของต้นไม้ ซึ่งไม่มีโหนดพ่อแม่ (parent node).
- Node (โหนด): แต่ละจุดในต้นไม้ที่สามารถเก็บข้อมูล และมีการเชื่อมโยงกับโหนดลูก (child nodes).
- Edge (ขอบ): เส้นทางที่เชื่อมโยงโหนดหนึ่งไปยังอีกโหนดหนึ่ง.
- Parent (พ่อแม่): โหนดที่มีโหนดอื่นเป็นลูก.
- Child (ลูก): โหนดที่เป็นลูกของโหนดอื่น.
- Leaf (ใบ): โหนดที่ไม่มีลูก หรือเป็นโหนดปลายของต้นไม้.
- Subtree (ต้นไม้ย่อย): ต้นไม้ที่เกิดจากโหนดย่อยในต้นไม้หลัก.

### Binary Tree:
<img width="1000" alt="BT" src="https://github.com/user-attachments/assets/d50f25a1-c57f-426f-9c5d-f025d0c12bae">  

- เป็นต้นไม้ที่แต่ละโหนดมีลูกได้ไม่เกิน 2 โหนด คือ โหนดซ้าย (Left Child) และโหนดขวา (Right Child).
- โครงสร้างนี้ทำให้การค้นหาหรือการทำงานกับข้อมูลง่ายขึ้นเพราะมีลำดับชั้นชัดเจน.

### Binary Search Tree (BST):

<img width="1000" alt="BST" src="https://skilled.dev/images/bst-visualize.gif">  

- เป็นต้นไม้ค้นหาแบบทวิภาค โดยข้อมูลที่น้อยกว่าจะถูกวางไว้ทางด้านซ้ายของโหนดปัจจุบัน ส่วนข้อมูลที่มากกว่าจะอยู่ทางด้านขวา.
- ประสิทธิภาพในการค้นหา แทรก หรือ ลบข้อมูลคือ O(log n) ในกรณีทั่วไป แต่ในกรณีที่ต้นไม้ไม่สมดุลจะทำให้ประสิทธิภาพลดลงไปเป็น O(n).

### AVL Tree:
![avl-tree](https://github.com/user-attachments/assets/a1b4e587-8d87-4355-ac6c-11421a718296)
<img width="924" alt="avl-tree_balnce2" src="https://github.com/user-attachments/assets/4ac19511-b95b-4d1c-b135-55341e5d6141">


- AVL Tree เป็น Binary Search Tree ที่ปรับสมดุลต้นไม้อัตโนมัติหลังจากมีการแทรกหรือลบโหนดใหม่.
- โครงสร้างของ AVL Tree มีการคำนวณ Balance Factor ซึ่งเป็นค่าต่างระหว่างความสูงของโหนดซ้ายและขวา โดยค่าที่อนุญาตคือ -1, 0, และ 1.
- เมื่อ Balance Factor เกินค่าที่กำหนด เช่น -2 หรือ 2 จะทำให้ต้นไม้ไม่สมดุล จึงต้องทำการหมุน (Rotation) เพื่อปรับสมดุล.

#### การหมุน (Rotations) ใน AVL Tree:

<img width="500" alt="Rotations" src="https://upload.wikimedia.org/wikipedia/commons/3/31/Tree_rotation_animation_250x250.gif">  

- Left Rotation: ใช้เมื่อต้นไม้หนักทางด้านขวา (Balance Factor < -1).
- Right Rotation: ใช้เมื่อต้นไม้หนักทางด้านซ้าย (Balance Factor > 1).
- Left-Right Rotation: ใช้เมื่อต้นไม้หนักทางซ้ายของลูกโหนดซ้าย (สองระดับ).
- Right-Left Rotation: ใช้เมื่อต้นไม้หนักทางขวาของลูกโหนดขวา (สองระดับ).

### วิธีการ Traversal:

1. Inorder Traversal: เรียงลำดับข้อมูลจากน้อยไปมาก โดยเรียงจากซ้าย ราก ขวา (Left-Root-Right).
<img width="600" alt="Inorder" src="https://miro.medium.com/v2/resize:fit:960/format:webp/1*nvZSw3M2Uq3EXOsc8Kd2Sw.gif">  

2. Preorder Traversal: เรียงลำดับโดยเริ่มจากรากก่อน ตามด้วยซ้ายและขวา (Root-Left-Right).
<img width="600" alt="Preorder" src="https://miro.medium.com/v2/resize:fit:960/1*Swjb2CWGQh55r9m7jEyg1Q.gif"> 

3. Postorder Traversal: เรียงลำดับจากซ้ายไปขวาแล้วจบที่ราก (Left-Right-Root).
<img width="600" alt="Postorder" src="https://miro.medium.com/v2/resize:fit:960/format:webp/1*4KpXD6en9pbN2mgbq4XraA.gif"> 

### การใช้งาน:
- Insertion: การเพิ่มข้อมูลใหม่ลงในต้นไม้ทำได้รวดเร็วและมีประสิทธิภาพ.
- Search: ค้นหาข้อมูลใน BST หรือ AVL Tree ทำได้อย่างมีประสิทธิภาพเนื่องจากโครงสร้างแบบทวิภาค.
- Deletion: การลบข้อมูลสามารถทำได้โดยไม่สูญเสียความสมดุลในต้นไม้, โดยเฉพาะใน AVL Tree ที่มีการหมุนเพื่อรักษาสมดุล.

## Graphs

- **กราฟ (Graphs)** เป็นโครงสร้างข้อมูลที่ประกอบด้วยชุดของโหนด (vertices) และเส้นเชื่อมระหว่างโหนด (edges) ซึ่งใช้ในการแทนความสัมพันธ์ต่างๆ ในการประมวลผลข้อมูล

  
<img width="500" alt="Screenshot 2567-09-19 at 16 26 27" src="https://github.com/user-attachments/assets/fa8c1871-8cc8-4dce-be6f-8ad97d78d91e"><img width="510" alt="Screenshot 2567-09-19 at 16 26 37" src="https://github.com/user-attachments/assets/9e40f798-de54-47c5-9a9d-227737b5835c">



### 1. กราฟแบบมีทิศทาง (Directed Graph) และกราฟแบบไม่มีทิศทาง (Undirected Graph)
- กราฟแบบมีทิศทาง (Directed Graph หรือ Digraph): เส้นเชื่อม (edges) ระหว่างโหนดจะมีทิศทาง กล่าวคือมีการระบุทิศทางการเชื่อมจากโหนดหนึ่งไปยังอีกโหนดหนึ่ง ตัวอย่างเช่นในกราฟของโซเชียลมีเดีย ผู้ใช้ A ติดตามผู้ใช้ B แต่ B อาจจะไม่ได้ติดตาม A กลับ
- กราฟแบบไม่มีทิศทาง (Undirected Graph): เส้นเชื่อมระหว่างโหนดไม่มีทิศทาง กล่าวคือสามารถเดินทางจากโหนด A ไปยังโหนด B หรือจาก B ไปยัง A ได้ทั้งสองทิศทาง ตัวอย่างเช่นในกราฟของเพื่อน คน A และคน B เป็นเพื่อนกันจึงเชื่อมต่อกันในทั้งสองทิศทาง

### 2. กราฟแบบมีน้ำหนัก (Weighted Graph) และกราฟแบบไม่มีน้ำหนัก (Unweighted Graph)
- กราฟแบบมีน้ำหนัก (Weighted Graph): แต่ละเส้นเชื่อม (edges) จะมีค่าน้ำหนักที่แตกต่างกัน เช่น ค่าความห่างไกล ค่าใช้จ่าย หรือเวลาในการเดินทางตัวอย่าง เช่น กราฟของเครือข่ายถนนที่เชื่อมระหว่างเมืองต่างๆที่มีระยะทางเป็นน้ำหนักของแต่ละเส้นเชื่อม
- กราฟแบบไม่มีน้ำหนัก (Unweighted Graph): ไม่มีค่าน้ำหนักบนเส้นเชื่อม เส้นเชื่อมจะมีค่าเท่ากันทั้งหมด

### 3. การแทนกราฟ (Graph Representation)
***กราฟสามารถแทนได้หลายวิธี***
- Adjacency Matrix: เป็นเมทริกซ์สองมิติที่แสดงความสัมพันธ์ระหว่างโหนด ถ้าโหนด i และ j มีเส้นเชื่อม เมทริกซ์จะมีค่าเป็น 1 (หรือเป็นค่าน้ำหนักในกรณีของกราฟแบบมีน้ำหนัก) ถ้าไม่มีเส้นเชื่อมจะเป็น 0
- Adjacency List: เป็นลิสต์ที่เก็บลิสต์ของโหนดที่เชื่อมต่อกัน ซึ่งมีประสิทธิภาพมากกว่าสำหรับกราฟขนาดใหญ่

### 4. การค้นหากราฟ (Graph Traversal)
***การเดินผ่านโหนดในกราฟสามารถทำได้สองวิธีหลัก***
- Breadth-First Search (BFS): การค้นหาแบบกว้าง จะเริ่มต้นจากโหนดหนึ่งและสำรวจโหนดทั้งหมดที่อยู่ใกล้เคียงก่อนแล้วจึงขยายไปยังโหนดที่อยู่ไกลขึ้น
- Depth-First Search (DFS): การค้นหาแบบลึก จะสำรวจเส้นทางจากโหนดหนึ่งไปจนสุดทางแล้วย้อนกลับมาตรวจสอบเส้นทางที่ยังไม่ได้สำรวจ

### 5. ประเภทกราฟ (Graph Types)
- Cyclic Graph: กราฟที่มีเส้นเชื่อมวนรอบกลับมาที่โหนดเริ่มต้น
- Acyclic Graph: กราฟที่ไม่มีวงรอบ
- Connected Graph: กราฟที่ทุกโหนดสามารถเชื่อมต่อกันได้
- Disconnected Graph: กราฟที่มีโหนดบางโหนดที่ไม่สามารถเชื่อมถึงกันได้


