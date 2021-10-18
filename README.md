# symmetric-encryption-modes

ให้นักศึกษาเขียน python program ที่ใช้ crypto library https://cryptography.io/en/latest/hazmat/primitives/symmetric-encryption โดยให้โปรแกรมที่เขียนมีการทำงานดังต่อไปนี้

1. ใช้ AES-128 ด้วยกุญแจลับ K = 0^128
2. เข้ารหัส message M1, M2, M3 ตามลำดับ โดยให้ค่าของ M1, M2, และ M3 เป็นไปตามที่ระบุดังต่อไปนี้

    2.1 ให้ id มีค่าเป็น Hex encoding ของ github username ของนักศึกษา เช่น หาก github username เป็น nchanath จะมีค่า id เป็น 6E6368616E617468
    2.2 ให้ M1 มีค่าเป็น ididid... จนกว่าจะได้ bitstring ที่มีความยาวใกล้ครบ 3 บล็อกให้ได้มากที่สุด จากนั้นให้เติม 0 ตามความจำเป็น จนกว่า bitstring ที่ได้จะมีความยาวเท่ากับ 3 บล็อกพอดี เรียก bitstring ที่ได้เป็นผลลัพธ์ในขั้นตอนนี้ว่า M1
    2.3 ให้ M2 มีค่าเป็น complement ของ M1
    2.4 ให้ M3 มีค่าเป็น M2 xor 1^256 0^128

3. พิมพ์ M1, M2, และ M3 ให้ครบทุกบิตออกทาง standard output โดยให้พิมพ์

    3.1 เฉพาะตัวข้อความ
    3.2 หนึ่งข้อความต่อ 1 บรรทัด
    3.3 และให้พิมพ์ในรูปแบบ hex string เท่านั้น ห้ามมีตัวอักษรอื่นปะปน

4. พิมพ์ ciphertexts ที่ได้จากการเข้ารหัสให้ครบทุกบิตออกทาง standard output โดยให้พิมพ์

    4.1 เฉพาะตัว ciphertexts
    4.2 หนึ่ง ciphertext ต่อ 1 บรรทัด
    4.3 และให้พิมพ์ในรูปแบบ hex string เท่านั้น ห้ามมีตัวอักษรอื่นปะปน

5. ถอดรหัส ciphertexts ในข้อ 4. แล้วแสดงผลลัพธ์ออกทาง standout output โดยให้พิมพ์

    5.1 เฉพาะผลลัพธ์
    5.2 หนึ่งผลลัพธ์ต่อ 1 บรรทัด
    5.3 และให้พิมพ์ในรูปแบบ hex string เท่านั้น ห้ามมีตัวอักษรอื่นปะปน

โดยให้นักศึกษาเขียนโปรแกรมดังกล่าว ที่ใช้วิธีการเข้ารหัสใน modes of operation ดังต่อไปนี้
1. ECB ให้ตั้งชื่อไฟล์ว่า ecb.py
2. CBC$ ให้ตั้งชื่อไฟล์ว่า cbca.py
3. CBCC ให้ตั้งชื่อไฟล์ว่า cbcb.py
4. CTR$ ให้ตั้งชื่อไฟล์ว่า ctra.py
5. CTRC ให้ตั้งชื่อไฟล์ว่า ctrb.py

โดยการทำงานในแต่ละ mode ให้เป็นไปตามที่ศึกษาในชั้นเรียน (ตามที่ระบุใน slides ที่ใช้ในชั้นเรียน)
