CREATE TABLE students (
         StudentID int NOT NULL AUTO_INCREMENT,
         Student_Name varchar(255),
         Father_Name varchar(255),
         Address varchar(255),
         State varchar(255),
         City varchar(255),
         Mobile_no varchar(20),
         Email_id varchar(255),
         Password varchar(255),
	 PRIMARY KEY (StudentID)
);
INSERT INTO students (Student_Name, Father_Name, Address,State, City, Mobile_no, Email_id, Password )
VALUES ('Jyanti', 'Satish Kumar', 'Manpur', 'Bihar', 'Gaya', '7665', 'pk81071@gmail.com', '123');

