# symmetric-encryption-modes

ให้นักศึกษาเขียน python โปรแกรม ที่ใช้ crypto library https://cryptography.io/en/latest/hazmat/primitives/symmetric-encryption โดยให้โปรแกรมที่เขียนมีการทำงานดังต่อไปนี้

1. ใช้ AES-128 ด้วยกุญแจลับ K = 0^128
2. เข้ารหัส message M ที่เป็นชื่อ (username) ของนักศึกษาในระบบ github.com ตามด้วย 0 จนกว่าจะเต็ม block
3. พิมพ์ message ทั้งหมดให้ครบทุกบิตออกทาง standard output ให้พิมพ์เฉพาะ message และให้พิมพ์ในรูปแบบ hex string เท่านั้น ห้ามมีตัวอักษรอื่นปะปน
4. พิมพ์ ciphertext ที่ได้จากการเข้ารหัสให้ครบทุกบิตออกทาง standard output ให้พิมพ์เฉพาะ ciphertext  และให้พิมพ์ในรูปแบบ hex string เท่านั้น ห้ามมีตัวอักษรอื่นปะปน
5. ถอดรหัส ciphertext ในข้อ 3. แล้วแสดงผลลัพธ์ออกทาง standout output ให้พิมพ์เฉพาะผลลัพธ์ และให้พิมพ์ในรูปแบบ hex string เท่านั้น ห้ามมีตัวอักษรอื่นปะปน

โดยให้นักศึกษาเขียนโปรแกรมดังกล่าว ที่ใช้วิธีการเข้ารหัสใน modes of operation ดังต่อไปนี้
1. ECB ให้ตั้งชื่อไฟล์ว่า ecb.py
2. CBC$ ให้ตั้งชื่อไฟล์ว่า cbca.py
3. CBCC ให้ตั้งชื่อไฟล์ว่า cbcb.py
4. CTR$ ให้ตั้งชื่อไฟล์ว่า ctra.py
5. CTRC ให้ตั้งชื่อไฟล์ว่า ctrb.py

โดยการทำงานในแต่ละ mode ให้เป็นไปตามที่ศึกษาในชั้นเรียน (ตามที่ระบุใน slides ที่ใช้ในชั้นเรียน)
