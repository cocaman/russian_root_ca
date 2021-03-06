# New Russian Root CA

> It will replace the foreign security certificate if it is revoked or expires. The Ministry of Digital Development will provide a free domestic analogue. The service is provided to legal entities - site owners upon request within 5 working days

## RootCa_SSL_RSA.zip
```
   Date      Time    Attr         Size   Compressed  Name
------------------- ----- ------------ ------------  ------------------------
2022-03-02 09:10:18 ....A         2090         1568  rootca_ssl_rsa2022.cer
2022-03-02 09:17:35 ....A         3944         1899  rootca_ssl_rsa2022.cer.detached.sig
------------------- ----- ------------ ------------  ------------------------
2022-03-02 09:17:35               6034         3467  2 files
```

Source: https://www.gosuslugi.ru/tls

# OSINT Resources
## CRT.SH
* Subject Key Identifier / Match: =    Search: 'e1d181e5ce5a5f04aad2e9b69d66b1c5faac2c87'
   * https://crt.sh/?ski=e1d181e5ce5a5f04aad2e9b69d66b1c5faac2c87
* CA ID/Match: =    Search: '235725'
   * https://crt.sh/?caid=235725
* Identity/Match: ILIKE    Search: '%'    Issuer CA ID: 235725
   * https://crt.sh/?Identity=%25&iCAID=235725
 
### Intermediate certificats
* Subject Key Identifier / Match: =    Search: 'd1e1710d0b2d814e6e8a4a8f4c23b34c5eab690b'
   * https://crt.sh/?ski=d1e1710d0b2d814e6e8a4a8f4c23b34c5eab690b
 
 ## Censys
 * Certificates with hash d26d2d0231b7c39f92cc738512ba54103519e4405d68b5bd703e9788ca8ecf31
   * https://search.censys.io/certificates/help?q=parsed.fingerprint_sha256%3Ad26d2d0231b7c39f92cc738512ba54103519e4405d68b5bd703e9788ca8ecf31
* Certificats with issuer `The Ministry of Digital Development and Communications`
   * https://search.censys.io/certificates?q=parsed.issuer_dn%3D%22C%3DRU%2C%20O%3DThe%20Ministry%20of%20Digital%20Development%20and%20Communications%2C%20CN%3DRussian%20Trusted%20Root%20CA%22
* Certificats with issuer `The Ministry of Digital Development and Communications` and `Russian Trusted Sub CA`
   * https://search.censys.io/certificates?q=parsed.issuer_dn%3D%22C%3DRU%2C+O%3DThe+Ministry+of+Digital+Development+and+Communications%2C+CN%3DRussian+Trusted+Sub+CA%22 

## CRL links
* http://reestr-pki.ru/cdp/rootca_ssl_rsa2022.crl
* http://company.rt.ru/cdp/rootca_ssl_rsa2022.crl
* http://rostelecom.ru/cdp/rootca_ssl_rsa2022.crl

# Known domains using the new root CA certificate
* https://ythm.ru/
   * https://zabbix.ythm.ru/
* https://bratsk.city/
* https://psi.promo.sber.ru/
* https://dev4.webquik-test.sberbank.ru/
* https://www.sberbank-com.os-psi.sberbank.ru/index
* https://www.ofukem.ru/
* https://sberkids-t.sberbank.ru/
* https://online.nrb.ru/
* https://cbro-t.sberbank.ru/
* https://geo-t.online.sberbank.ru/

