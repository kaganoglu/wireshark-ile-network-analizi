### ARP Filtreleri
Arp, yerel ağda IP adresine ait MAC adresinin bulunmasını sağlayan bir ağ protokolüdür. Her cihazın ARP tablosu vardır.

`arp`

------------

Arp protokolüne ait paketleri filtrelemek için kullanılır.

`arp.opcode == 1`

Arp sorgusunun ilk işlemine request denir. Arp protokolünde request paketleri filtrelemek için kullanılır.

`arp.opcode == 2`

------------

Ayakta olan ve gelen isteğe cevap veren cihazların gönderdiği Arp reply paketleri listelemek için kullanılır.

`arp.src.hw_mac == "68-7F-74-12-34-56"`

Arp paketleri içerisinde kaynak mac adresi filtrelemek için kullanılır.

`arp.src.proto_ipv4 == "192.168.1.3"`

Arp paketleri içerisinde kaynak IP adresi filtrelemek için kullanılır.

------------

`arp.dst.hw_mac == "68-7F-74-12-34-56"`

Arp paketleri içerisinde hedef mac adresi filtrelemek için kullanılır.

`arp.dst.proto_ipv4 == "192.168.1.3" `

Arp paketleri içerisinde hedef IP adresi filtrelemek için kullanılır.

------------
