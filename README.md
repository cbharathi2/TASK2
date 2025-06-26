# TASK2
#INSERT FOR ADDING ROWS:

INSERT INTO authors (name) VALUES ('George Orwell');
INSERT INTO categories (category_name) VALUES 
  ('Dystopian'),
  ('Biography');
  INSERT INTO books 
  (title, author_id, category_id, isbn, publication_year, copies_available)
VALUES 
  ('1984', 2, 1, '9780451524935', 1949, 3);
INSERT INTO books 
  (title, author_id, category_id, isbn, publication_year)
VALUES 
  ('Animal Farm', 2, 1, '9780451526342', 1945);

#HANDLE MISSING VALUE:
INSERT INTO members (name, email, phone, membership_date)
VALUES ('Alice Smith', NULL, NULL, CURDATE());


#Use UPDATE and DELETE with WHERE:

UPDATE books
SET copies_available = copies_available + 2
WHERE title = '1984';

UPDATE authors
SET bio = 'English author of 1984 and Animal Farm'
WHERE name = 'George Orwell';

DELETE FROM categories
WHERE category_name = 'Biography';


#DELETE
DELETE FROM members
WHERE member_id = 1;
