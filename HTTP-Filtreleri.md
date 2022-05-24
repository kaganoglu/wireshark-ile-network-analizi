### HTTP Filtreleri
Bu bölümde ise http için kullanılabilecek bazı filtrelerden bahsedeceğim.

------------
`http`

HTTP protokolüne ait tüm paketleri filtreler.

------------

`http.request`

Tüm HTTP isteklerini içeren paketleri filtreler.

------------

`http.request.method == "GET"`

`http.request.method == "POST"`

`http.request.method == "PUT"`

`http.request.method == "HEAD"`

`http.request.method == "DELETE"`

`http.request.method == "PATCH"`

`http.request.method == "OPTIONS"`

HTTP isteklerinde kullanılan metotlara ait paketleri filtrelemek için kullanılır.

------------

`http.request.uri == "http://kaganoglu.com/"`

Belirlenen bir web sitesine gönderilen veya alınan paketleri filtrelemek için kullanılır.

------------

`http.request.uri contains "batuhan"`

URL kısmında belirtilen değeri içeren paketleri filtrelemek için kullanılır.

------------

`http.response.code == 200`

`http.response.code == 404`

`http.response.code == 302`

HTTP yanıt kodlarına göre filtreleme yapmak için kullanılır.

------------

`http.host == "kaganoglu.com"`

Spesifik bir web sitesine yapılan istekleri içeren paketleri filtrelemek için kullanılır.

------------

`http.host contains "batuhan"`

Belirli bir kelimeyi içeren web sitelerine yapılan istekleri filtrelemek için kullanılır.

------------

`http.referer == "http://kaganoglu.com/"`

Referer adresleri filterelemek için kullanılır.

------------

`http contains image`

HTTP protokolüne ait paketlerde içinde image stringi olan paketleri filtrelemek için kullanılır.

------------

`http.content_type[0:4] == "text"`

HTTP protokolüne ait paketlerde içinde dosya türü "text" ile başlayan paketleri filtrelemek için kullanılır.
