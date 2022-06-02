### FTP Filtreleri
Bu bölümde ise FTP için kullanılabilecek bazı filtrelerden bahsedeceğim.

------------
`ftp`

FTP protokolüne ait tüm paketleri filtreler. 

`tcp.dstport == 21`

FTP, TCP protokolünün 21 numaralı portunu kullandığı için bu filtreyi de kullanabiliriz.

------------

`ftp.request`

Tüm HTTP isteklerini içeren paketleri filtreler.

------------

`ftp.request.command`

FTP protokolünde kullanılan komutları içeren paketleri filtrelemek için kullanılır.

`ftp.request.command = USER`

`ftp.request.command = PASS`

FTP kullanıcılarına ait kullanıcı adı ve parola bilgilerinin bulunduğu paketleri filtrelemek için kullanılır.

------------

`ftp.response.code == 230`

`ftp.response.arg == "Login successful."`

Başarılı giriş işlemlerine ait paketleri filtrelemek için kullanılır.

`ftp.response.code == 226`

`ftp.response.arg == "ABOR"`

Dosya transferlerine ait olan paketleri filtrelemek için kullanılır.
