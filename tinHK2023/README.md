# Đáp án:
## Trắc nghiệm
	1.C
	2.B
	3.D
	4.D
	5.A
	6.D
	7.C
	8.A
	9.D
	10.B
	11.B
	12.A
	13.A
	14.B
	15.C
	16.A
	17.B
	18.A
	19.B
	20.B
	21.A
	22.B
	23.C
	24.A
	25.B
	26.A
	27.C
	28.C
## Tự luận:
	Câu 1. Danh sách trường khoá: Mã môn học, (Mã môn học, Môn học).
 		Khoá chính: Mã môn học.
	Câu 2. Danh sách các khoá: Mã học sinh,Số CCCD và tất cả các nhóm trường chứa ít nhất một trong hai trường Mã học sinh, Số CCCD.
		Có thể chọn Khoá chính là: Mã học sinh hay số CCCD.
	Câu 3. Danh sách khoá: (Mã học sinh, Mã môn học), (Mã học sinh, Mã môn điểm).
		Khoá chính: (Mã học sinh, Mã môn học).
	Câu 4. Mã môn học là khoá ngoài của bảng C, tham chiếu đến khoá chính của bảng A.
		Nếu chọn Mã học sinh là khoá chính của bảng B thì Mã học sinh là khoá ngoài của bảng C, tham chiếu đến khoá chính của bảng B
	Câu 5. Danh sách khoá: Số đăng kí, (Số khung, số máy), tất cả các nhóm trường có chứa ít nhất một trong hai khoá Số đăng kí và  (Số khung, số máy). 
		Khoá chính: Số đăng kí.
	Câu 6. Số CCCD
	Câu 7. Bảng E có khoá ngoài Số đăng kí tham chiếu đến khoá chính của bảng D
	Câu 8. 
```sql
CREATE TABLE monhoc (
	mamh CHAR (5),
	tenmh VARCHAR (64),
	
);
ALTER TABLE monhoc ADD PRIMARY KEY (mamh);
```
Câu 9.
```sql
CREATE TABLE hocsinh (
	mahs 	 CHAR (6),
	cccd 	 CHAR (12),
	hoten 	 VARCHAR (64),
	ngsinh DATE,
	gt	 CHAR (1),	
);
ALTER TABLE hocsinh ADD PRIMARY KEY (mahs);
```
Câu 10.
```sql
ALTER TABLE hocsinh 
CHANGE COLUMN ngsinh ngaysinh DATE;
```
Câu 11.
```sql
CREATE TABLE diemmonhoc (
	mahs 	 CHAR (6),
	mamh	 CHAR (5),
	diem 	 INT,
	ngsinh DATE,
	PRIMARY KEY (mahs, mamh),	
);
ALTER TABLE ADD FOREGIN KEY hs REFERENCES hocsinh (mahs);
ALTER TABLE ADD FOREGIN KEY mh REFERENCES monhoc(mamh);
ALTER TABLE ADD CONSTRAINT dm CHECK (diem BETWEEN0 AND 10);
```
Câu 12. 
```sql
INSERT INTO monhoc VALUES
	(‘MAT10’, ‘Toán học’),
	(‘MAT11’, ‘Toán học’),
	(‘PHY10’, ‘Vật lí’),
	(‘PHY11’, ‘Vật lí’),
	(‘LIT10’, ‘Ngữ văn’);
 ```
Câu 13.
```sql
UPDATE monhoc
SET tenmh = ‘Toán học’
WHERE mamh = ‘MAT10’ OR mamh = ‘MAT 11’;
```
Câu 14.
```sql
DELETE FROM monhoc WHERE mamh = ‘LIT10’;
```
Câu 15. 
```sql
SELECT * FROM monhoc;
```
Câu 16. 
```
SELECT * FROM monhoc WHERE tenmh = ‘Toán học’;
```
