# SQL_Traine1

#Query 1
select * from customers;
<img width="766" alt="image" src="https://user-images.githubusercontent.com/78079556/236471841-cd0ee5d9-96e8-40ec-aff2-5d6d87620388.png">
keterangan: Memunculkan seluruh data yang ada pada table customers.

#Query 2
SELECT creditLimit FROM customers ORDER BY creditLimit DESC;
<img width="449" alt="image" src="https://user-images.githubusercontent.com/78079556/236475817-39dbc1e3-a7c5-4529-b08b-1f3e08682914.png">
keterangan: Dari table customers untuk Memunculkan data credit limit customer dari terbawah / Menurun.

#Query 3
SELECT customerName,phone,addressLine1,city,country FROM customers WHERE country = 'USA' ORDER BY customerName;
<img width="468" alt="image" src="https://user-images.githubusercontent.com/78079556/236474448-c6c26718-90b9-4abb-907b-c75e7f0c8509.png">
keterangan: Dari table customers untuk memunculkan data kolom customerName, phone, addressLine1,City,country dengan kolom country yang berisikan USA.

#Query 4
SELECT customerName, phone, addressLine2, city, country, creditLimit FROM customers WHERE creditLimit > 90000 AND country = 'USA' ORDER BY creditLimit DESC;
<img width="677" alt="image" src="https://user-images.githubusercontent.com/78079556/236477885-5435c5fe-473e-453a-9ebe-ffbfd4ca0835.png">
keterangan: Dari table customers untuk memunculkan data kolom customerName, phone, addressLine2,City,country, creditLimit dengan nilai creditlimit diatas 90000,
county = USA dan dari kolom creditlimt dengan data terbesar.

#Query 5
SELECT c.customerNumber as 'order_id', c.contactFirstName as 'Customer_Name', c.country, o.orderNumber, o.orderDate
FROM customers as c
inner join orders as o on c.customerNumber = o.customerNumber 
where c.creditLimit > 100000
ORDER BY contactFirstName;

<img width="745" alt="image" src="https://user-images.githubusercontent.com/78079556/236692571-9f8db798-e6d6-4d70-a471-6c8c9540246e.png">
keterangan: Dari table customers dihubungkan dengan table orders dengan relasi kolom customerNumber di table customers dan kolom customerNumber di table orders
untuk menampilkan data kolom cutomerNumber table customer, kolom contactFirstName table customers, kolom country table customer, kolom orderNumber table orders, dan kolom orderDate table orders berdasarkan kolom creditLimi table customers dengan nilai diatas 100000 dan diurutkan berdasarkan value kolom contactFirstName.

#Query 6
CREATE UNIQUE INDEX index_orders ON orders (orderNumber);

<img width="338" alt="image" src="https://user-images.githubusercontent.com/78079556/236693820-dae2c11a-ec0b-4e69-87ed-5b1e0a375bb5.png">
keterangan: Create index pada table orders di kolom orderNumber dengan tipe UNIQUE (tidak memperbolehkan nilai duplikat).

show index from orders;
<img width="713" alt="image" src="https://user-images.githubusercontent.com/78079556/236694304-411f0d40-f00c-4a44-94cf-e5e860cbc8be.png">

