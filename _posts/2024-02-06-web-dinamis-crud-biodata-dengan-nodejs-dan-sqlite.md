
Berikut ini adalah contoh kode keseluruhan untuk membuat aplikasi web dinamis biodata siswa dengan Node.js, SQLite, dan operasi CRUD. Pastikan Anda telah membuat struktur proyek seperti yang dijelaskan sebelumnya:

Buat file app.js:
javascript
Copy code
const express = require('express');
const sqlite3 = require('sqlite3');
const bodyParser = require('body-parser');

const app = express();
const port = 3000;

const db = new sqlite3.Database('./database.db');

app.use(bodyParser.urlencoded({ extended: true }));

// Create Table
db.serialize(() => {
  db.run('CREATE TABLE IF NOT EXISTS biodata (id INTEGER PRIMARY KEY, nama TEXT, usia INTEGER)');
});

// Read
app.get('/', (req, res) => {
  db.all('SELECT * FROM biodata', (err, rows) => {
    if (err) {
      return res.status(500).send(err.message);
    }
    res.render('index.html', { rows });
  });
});

// Create
app.post('/siswa', (req, res) => {
  const { nama, usia } = req.body;
  db.run('INSERT INTO biodata (nama, usia) VALUES (?, ?)', [nama, usia], (err) => {
    if (err) {
      return res.status(500).send(err.message);
    }
    res.redirect('/');
  });
});

// Update
app.put('/siswa/:id', (req, res) => {
  const { nama, usia } = req.body;
  const id = req.params.id;
  db.run('UPDATE biodata SET nama=?, usia=? WHERE id=?', [nama, usia, id], (err) => {
    if (err) {
      return res.status(500).send(err.message);
    }
    res.redirect('/');
  });
});

// Delete
app.delete('/siswa/:id', (req, res) => {
  const id = req.params.id;
  db.run('DELETE FROM biodata WHERE id=?', [id], (err) => {
    if (err) {
      return res.status(500).send(err.message);
    }
    res.redirect('/');
  });
});

// Server Configuration
app.set('view engine', 'html');
app.use(express.static('public'));

// Server Start
app.listen(port, () => {
  console.log(`Server is running at http://localhost:${port}`);
});
Buat folder views dan buat dua file HTML, yaitu index.html dan form.html. Isi sesuai dengan kebutuhan Anda.

Jalankan perintah npm install untuk menginstal modul-modul yang diperlukan.

Jalankan aplikasi dengan perintah node app.js.

Dengan langkah-langkah ini, Anda akan memiliki aplikasi web sederhana yang memungkinkan Anda untuk menambahkan, mengedit, dan menghapus biodata siswa. Pastikan untuk menyesuaikan tampilan dan logika bisnis sesuai dengan kebutuhan proyek Anda.



