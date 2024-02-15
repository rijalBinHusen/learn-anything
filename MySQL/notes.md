## mengganti password root mysql
- masuk ke mysql dulu

```sql
mysql -u root -p passwordNya/atauBiarkanKosongJikaBelumAdaPassword
```

## Create new password
```sql
ALTER USER 'root'@'localhost' IDENTIFIED BY 'MyN3wP4ssw0rd';
flush privileges;
exit;
```

## Create full text index
Create a full-text index on an existing column in a MySQL database. This will allow you to search for words and phrases in the column more efficiently.
To create a full-text index, you can use the CREATE FULLTEXT INDEX statement. For example, the following statement creates a full-text index on the content column of the articles table:
```sql
CREATE FULLTEXT INDEX ft_idx_articles_content ON articles (content); 

// create index or alter as unique
ALTER TABLE binhusenstore_orders ADD UNIQUE(id);
CREATE INDEX binhusenstore_orders_id_group ON binhusenstore_orders (id_group);

CREATE INDEX binhusenstore_payments_order_id_group ON binhusenstore_payments (id_order_group);
CREATE INDEX binhusenstore_payments_order_id ON binhusenstore_payments (id_order);
```
