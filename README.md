
Twitterbot
Twitterbot adalah aplikasi Python sederhana untuk:

membaca dan mengurai umpan RSS serta memposting judul dan tautannya ke akun Twitter.
mencari tweet untuk kata kunci atau hashtag dan me-retweet tweet tersebut.
Kedua fungsi (Membaca RSS dan me-retweet) dapat digunakan secara independen. Bot terbatas untuk menangani satu umpan dan satu akun Twitter.

Install
Unduh atau git clone Twitterbot:
git clone https://github.com/peterdalle/twitterbot
Instal dependensi feedparser dan twython:
pip instal feedparser
pip instal twython
Buat aplikasi Twitter, dan buat kunci, token, dll.
Ubah pengaturan di kode sumber.
Ubah feed_url menjadi RSS feed yang ingin Anda baca.
Ubah variabel di kelas TwitterAuth dan tambahkan kunci, token, dll. Untuk menghubungkan ke aplikasi Twitter Anda.
Ubah retweet_include_words untuk kata kunci yang ingin Anda cari dan retweet, dan retweet_exclude_words untuk kata kunci yang ingin Anda kecualikan dari retweet. Misalnya retweet_include_words = ["foo"] dan retweet_exclude_words = ["bar"] akan menyertakan tweet apapun dengan kata "foo", selama kata "bar" tidak ada. Daftar ini juga boleh dikosongkan, misalnya retweet_exclude_words = [].
Persyaratan
Python 3+
Akun Twitter
Pemakaian
Baca RSS feed dan posting ke akun Twitter:

$ python twitterbot.py rss
Cari tweet dan retweet:

$ python twitterbot.py rt
Siapkan contoh crontab
Lebih disukai, Anda harus menggunakan crontab untuk mengatur Twitterbot agar berjalan sesuai jadwal.

contoh crontab:

# Baca RSS feed setiap jam dan tweet tautan baru.
00 * * * * python twitterbot.py rss

# Rewteet kata kunci / tagar setiap 15 menit.
* / 15 * * * * python twitterbot.py rt
Gunakan editor ekspresi jadwal cron untuk membuat cron dengan mudah.

Pertanyaan
Lihat Pertanyaan dan jawaban di wiki.
