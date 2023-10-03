# Specifications Emas Rutin


## Get JWT Token

```bash
curl --request POST \
--url http://10.0.118.39:5556/gateway/security/getJsonWebToken \
--header 'Content-Type: application/json' \
--header 'X-Gateway-APIKey: b30d1f40-68c5-4ed5-b55e-85be3af7aa57' \
--data '{
    "claimsSet": {
        "appId": "525b3a61-8968-479d-9a45-9120bf614471"
    }
}'
```

- Request

```json
{
  "claimsSet": {
    "appId": "525b3a61-8968-479d-9a45-9120bf614471"
  }
}
```

- Response
```json
{
  "expiresIn": 30000,
  "tokenType": "Bearer",
  "accessToken": "eyJraWQiOiJzc29zIiwiYWxnIjoiUlM1MTIifQ.eyJzdWIiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS05MTIwYmY2MTQ0NzEiLCJhdWQiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS05MTIwYmY2MTQ0NzEiLCJhcHBJZCI6IjUyNWIzYTYxLTg5NjgtNDc5ZC05YTQ1LTkxMjBiZjYxNDQ3MSIsImlzcyI6IkFQSUdXIiwiZXhwIjoxNjk0NjAzOTQ5LCJpYXQiOjE2OTQ1NzM5NDl9.KLcK8xzVE2SERCHDaqbV8f02mprnaP3_p2Gh1l4QM6sfpqvePvqsKVq8aTbnWNXhot09sDQAHdgbfYFvXEFLfEiRcchZPG4mwTsBPPO-RfUCMf80qr9KYz0Xia8r1zoSUvx1vhHkbzTi7SnKnH6QdCpd6t0SkoqVrThUL1iamMnhmj5YvwdqAj0T1hZyzJ0ZUp_IS98R1k8zihrLla3p0KHbzHwpnFc14S3ShnpMRpe-XejZnbFg6sSL4Dc6jwgk_9_4PLcNntTODzadtVzcLv21S6VwoRQDpYQkcsJ145kK1AUiV95bv46W35jlCp8SlCM083fem6EkmzPQFT_g"
}
```

## Register Emas Sumber Tabungan

```bash
curl --request POST \
--url http://10.0.118.39:5556/gw-autoemas-api/v1/registerEmasTabungan \
--header 'Authorization: Bearer 
eyJraWQiOiJzc29zIiwiYWxnIjoiUlM1MTIifQ.eyJzdWIiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS0
5MTIwYmFkYjYxNDQ3MSIsImF1ZCI6IjUyNWIzYTYxLTg5NjgtNDc5ZC05YTQ1LTkxMjBiZjYxNDQ3MSIsInN
1YiI6IjUyNTg4OTZhLTIzZDQtNDY0My05ZTQ0LWJmZmRmN2ViYWMyMSIsImlzcyI6ImFwcGlvdG8iLCJleHAiOj
E2OTUwNzU4MjAsImlhdCI6MTY5NTA2OTgyMH0.D7n6q1SUNmkiOJPRn2p_T2qKv9ELtOjmLhWn45RCS5eMoXOu1lAe8
2xXzvOR1f1GL-EDTC-xWfyQv2oIj6lw_6DGLCOUGDWXHQvADGo58Ewxd5s0oLfOg88vcm6B9RXD0Mp4TmeVlh_RtiHnWzKAOosw
5B26xDPTR3N5T1qmBOeVlf-rtr93JF1UNyo7IVy9vYr25ssU2sPgJdciIsx8Sc-hbSsCfn5sMP4Dvfg0r8l8lbw-2FBXWk
wW09Q1YSyIDKJLSzqil57qr2kMc_Osfz-W6zE7sFuDnL6Q0JlL-XmiQhAeJ95J_GITm3HeD3-JvRwL2qrh8lT9WAEfQw' \
--header 'Content-Type: application/json' \
--header 'User-Agent: insomnia/2023.5.8' \
--data '{
"idRegistration": "f3964df9-1358- 4a4b-9bdc-6025c20b969c",
"nama": "MOHAMAD MARZUKI",
"noRekeningEmas": "8803156968",
"noRekeningDebit": "7225322206",
"amount": 50500,
"channel": "MBG",
"bulanAwal": 10,
"jangkaBulan": 1,
"tanggal": "10",
"status": true,
"cif": "90047219",
"tanggalBerhenti": "2025-10"
}'
```

- Request
```json
{
  "idRegistration": "f3964df9-1358- 4a4b-9bdc-6025c20b969c",
  "nama": "MOHAMAD MARZUKI",
  "noRekeningEmas": "8803156968",
  "noRekeningDebit": "7225322206",
  "amount": 50500,
  "channel": "MBG",
  "bulanAwal": 10,
  "jangkaBulan": 1,
  "tanggal": "10",
  "status": true,
  "cif": "90047219",
  "tanggalBerhenti": "2025-10"
}
```

- Response
```json
{
  "success": true,
  "message": "Success",
  "code": "00",
  "payload": {
    "registrationId": "d649f91a-a850-4bdd-9925-0329a9928e9b"
  }
}
```

## Register Emas Sumber Bagi Hasil

```bash
curl --request POST \
--url http://10.0.118.39:5556/gw-autoemas-api/v1/reigsterEmasBagiHasil \
--header 'Authorization: Bearer eyJraWQiOiJzc29zIiwiYWxnIjoiUlM1MTIifQ.eyJzdWIiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS0
5MTIwYmY2MTQ0NzEiLCJhdWQiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS05MTIwYmY2MTQ
0NzEiLCJhcHBJZCI6IjUyNWIzYTYxLTg5NjgtNDc5ZC05YTQ1LTkxMjBiZjYxNDQ3MSIsImlzcyI6IkFQS
UdXIiwiZXhwIjoxNjk0Njg4NjI0LCJpYXQiOjE2OTQ2NTg2MjR9.g4BMsZ7eUk75cW57xmBoUtzQsgSi-HinY7wrCBIm-322H7b53VQW9HQAdOY9bGxU3Pn_6vgTp0uNcxN9O10-
lUK2YwLtfehZ0w-Gn6qc2uifsBDHgKKVCZvo4ansJ7RURB1ZY_avCEO6eaExcPhf-2RPE3HNAtz48MykrDA_1BkqR9cjQZU0bcVdVLNwYHnZg8bsRtAs5p8hENsU5hS1cQu9kJxQrGzN2Gi0
5eoFf9XbLepgqHUEIBICiB310eBKYzS-CFD2mF7nQIB6eOISfDDR0-3onR8fdlDRVq3oKObDS_0Lb7lQ4XkiWthpz1FlpWfLbYnMl4QBVeqw_hA' \
--header 'Content-Type: application/json' \
--header 'User-Agent: insomnia/2023.5.8' \
--data '{
"nama": "MOHAMAD MARZUKI",
"noRekeningEmas": "8803156968",
"noRekeningDebit": "7225322206",
"channel": "MBG",
"tanggalBerhenti": "2025-02"
}'
```

- Request
```json
{
  "nama": "MOHAMAD MARZUKI",
  "noRekeningEmas": "8803156968",
  "noRekeningDebit": "7225322206",
  "channel": "MBG",
  "tanggalBerhenti": "2025-02"
}
```

- Response

```json
{
  "success": true,
  "message": "Success",
  "code": "00",
  "payload": {
    "registrationId": "d649f91a-a850-4bdd-9925-0329a9928e9b"
  }
}
```

## Update Emas Rutin Sumber Tabungan

```bash
curl --request PUT \
--url http://10.0.118.39:5556/gw-autoemas-api/v1/updateEmasTabungan \
--header 'Authorization: Bearer 
eyJraWQiOiJzc29zIiwiYWxnIjoiUlM1MTIifQ.eyJzdWIiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS0
5MTIwYmY2MTQ0NzEiLCJhdWQiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS05MTIwYmY2MTQ
0NzEiLCJhcHBJZCI6IjUyNWIzYTYxLTg5NjgtNDc5ZC05YTQ1LTkxMjBiZjYxNDQ3MSIsImlzcyI6IkFQS
UdXIiwiZXhwIjoxNjk0Njg4NjI0LCJpYXQiOjE2OTQ2NTg2MjR9.g4BMsZ7eUk75cW57xmBoUtzQsgSi-HinY7wrCBIm-322H7b53VQW9HQAdOY9bGxU3Pn_6vgTp0uNcxN9O10-
lUK2YwLtfehZ0w-Gn6qc2uifsBDHgKKVCZvo4ansJ7RURB1ZY_avCEO6eaExcPhf-2RPE3HNAtz48MykrDA_1BkqR9cjQZU0bcVdVLNwYHnZg8bsRtAs5p8hENsU5hS1cQu9kJxQrGzN2Gi0
5eoFf9XbLepgqHUEIBICiB310eBKYzS-CFD2mF7nQIB6eOISfDDR0-3onR8fdlDRVq3oKObDS_0Lb7lQ4XkiWthpz1FlpWfLbYnMl4QBVeqw_hA' \
--header 'Content-Type: application/json' \
--header 'User-Agent: insomnia/2023.5.8' \
--data '{
"idRegistration": "f3964df9-1358-4a4b-9bdc-6025c20b969c",
"nama": "",
"noRekeningEmas": "",
"noRekeningDebit": "",
"amount": 70000,
"channel": "",
"bulanAwal": 2,
"jangkaBulan": 1,
"tanggal": "",
"status": true,
"cif": "",
"tanggalBerhenti": "2025-09"
}'
```

- Request
```json
{
  "idRegistration": "f3964df9-1358-4a4b-9bdc-6025c20b969c",
  "nama": "",
  "noRekeningEmas": "",
  "noRekeningDebit": "",
  "amount": 70000,
  "channel": "",
  "bulanAwal": 2,
  "jangkaBulan": 1,
  "tanggal": "",
  "status": true,
  "cif": "",
  "tanggalBerhenti": "2025-09"
}
```
- Response

```json
{
  "success": true,
  "message": "Success",
  "code": "00",
  "payload": {
    "idRegistration": "f3964df9-1358-4a4b-9bdc-6025c20b969c",
    "cif": null,
    "noRekeningEmas": "7001305399",
    "nama": "IGUH WIDIPANGESTU",
    "noRekeningDebit": "7001305338",
    "amount": 70000,
    "channel": "MBG",
    "bulanAwal": 2,
    "jangkaBulan": 1,
    "tanggal": "10",
    "active": true,
    "createdAt": "2023-08-28T07:12:09.000+00:00",
    "updatedAt": "2023-08-28T10:39:59.746+00:00",
    "tanggalBerhenti": "2025-09"
  }
}
```

## Berhenti Emas Rutin sumber Tabungan secara Otomatis

```bash
curl --request DELETE \
--url 'http://10.0.118.39:5556/gw-autoemasapi/v1/berhentiEmasTabunganOtomatis/?registrationId=f3964df9-1358-4a4b-9bdc6025c20b969c' \
--header 'Authorization: Bearer 
eyJraWQiOiJzc29zIiwiYWxnIjoiUlM1MTIifQ.eyJzdWIiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS0
5MTIwYmY2MTQ0NzEiLCJhdWQiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS05MTIwYmY2MTQ
0NzEiLCJhcHBJZCI6IjUyNWIzYTYxLTg5NjgtNDc5ZC05YTQ1LTkxMjBiZjYxNDQ3MSIsImlzcyI6IkFQS
UdXIiwiZXhwIjoxNjk0Njg4NjI0LCJpYXQiOjE2OTQ2NTg2MjR9.g4BMsZ7eUk75cW57xmBoUtzQsgSi-HinY7wrCBIm-322H7b53VQW9HQAdOY9bGxU3Pn_6vgTp0uNcxN9O10-
lUK2YwLtfehZ0w-Gn6qc2uifsBDHgKKVCZvo4ansJ7RURB1ZY_avCEO6eaExcPhf-2RPE3HNAtz48MykrDA_1BkqR9cjQZU0bcVdVLNwYHnZg8bsRtAs5p8hENsU5hS1cQu9kJxQrGzN2Gi0
5eoFf9XbLepgqHUEIBICiB310eBKYzS-CFD2mF7nQIB6eOISfDDR0-3onR8fdlDRVq3oKObDS_0Lb7lQ4XkiWthpz1FlpWfLbYnMl4QBVeqw_hA' \
--header 'Content-Type: application/json' \
--header 'User-Agent: insomnia/2023.5.8'
```

- Request : tidak ada request body

- Response Positive
```
Berhasil berhentikan beli emas bagi hasil otomatis id : f3964df9-1358-4a4b-9bdc-6025c20b969c!
```

- Response Negative

```json
{
  "responseCode": "01",
  "responseMessage": "Failed",
  "errorCode": "EMS-99-404",
  "errorMessage": "Not Found"
}
```

## Berhenti Emas Rutin sumber Bagi Hasil secara Otomatis

```bash
curl --request DELETE \
--url 'http://10.0.118.39:5556/gw-autoemasapi/v1/berhentiEmasBagiHasilOtomatis/?registrationId=f3964df9-1358-4a4b-9bdc6025c20b969c' \
--header 'Authorization: Bearer 
eyJraWQiOiJzc29zIiwiYWxnIjoiUlM1MTIifQ.eyJzdWIiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS0
5MTIwYmY2MTQ0NzEiLCJhdWQiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS05MTIwYmY2MTQ
0NzEiLCJhcHBJZCI6IjUyNWIzYTYxLTg5NjgtNDc5ZC05YTQ1LTkxMjBiZjYxNDQ3MSIsImlzcyI6IkFQS
UdXIiwiZXhwIjoxNjk0Njg4NjI0LCJpYXQiOjE2OTQ2NTg2MjR9.g4BMsZ7eUk75cW57xmBoUtzQsgSi-HinY7wrCBIm-322H7b53VQW9HQAdOY9bGxU3Pn_6vgTp0uNcxN9O10-
lUK2YwLtfehZ0w-Gn6qc2uifsBDHgKKVCZvo4ansJ7RURB1ZY_avCEO6eaExcPhf-2RPE3HNAtz48MykrDA_1BkqR9cjQZU0bcVdVLNwYHnZg8bsRtAs5p8hENsU5hS1cQu9kJxQrGzN2Gi0
5eoFf9XbLepgqHUEIBICiB310eBKYzS-CFD2mF7nQIB6eOISfDDR0-3onR8fdlDRVq3oKObDS_0Lb7lQ4XkiWthpz1FlpWfLbYnMl4QBVeqw_hA' \
--header 'User-Agent: insomnia/2023.5.8'
```

- Request : tidak ada request body

- Response Positive :

```
Berhasil berhentikan beli emas bagi hasil otomatis id : f3964df9-1358-4a4b-9bdc-6025c20b969c!
```

- Response Negative : 

```json
{
  "responseCode": "01",
  "responseMessage": "Failed",
  "errorCode": "EMS-99-404",
  "errorMessage": "Not Found"
}
```

## Ambil Portfolio Tabungan yang Ada Bagi Hasil berdasarkan CIF

```bash
curl --request GET \
--url 'http://10.0.118.39:5556/gw-autoemasapi/v1/inquiry/getCifPortofolioForEmasBagiHasil?cif=7300584' \
--header 'Authorization: Bearer 
eyJraWQiOiJzc29zIiwiYWxnIjoiUlM1MTIifQ.eyJzdWIiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS0
5MTIwYmY2MTQ0NzEiLCJhdWQiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS05MTIwYmY2MTQ
0NzEiLCJhcHBJZCI6IjUyNWIzYTYxLTg5NjgtNDc5ZC05YTQ1LTkxMjBiZjYxNDQ3MSIsImlzcyI6IkFQS
UdXIiwiZXhwIjoxNjk0Njg4NjI0LCJpYXQiOjE2OTQ2NTg2MjR9.g4BMsZ7eUk75cW57xmBoUtzQsgSi-HinY7wrCBIm-322H7b53VQW9HQAdOY9bGxU3Pn_6vgTp0uNcxN9O10-
lUK2YwLtfehZ0w-Gn6qc2uifsBDHgKKVCZvo4ansJ7RURB1ZY_avCEO6eaExcPhf-2RPE3HNAtz48MykrDA_1BkqR9cjQZU0bcVdVLNwYHnZg8bsRtAs5p8hENsU5hS1cQu9kJxQrGzN2Gi0
5eoFf9XbLepgqHUEIBICiB310eBKYzS-CFD2mF7nQIB6eOISfDDR0-3onR8fdlDRVq3oKObDS_0Lb7lQ4XkiWthpz1FlpWfLbYnMl4QBVeqw_hA' \
--header 'User-Agent: insomnia/2023.5.8'
```

- Request : tidak ada request body nya

- Response Positive : 
```json
[
  {
    "accountNumber": "7234537851",
    "accountName": "IGUH WIDIPANGESTU",
    "desc": "Tab Investasi Terikat (Mudh Muqayy)",
    "currency": "IDR",
    "category": "6018",
    "ammountAutoSave": 0,
    "registerStatus": "N"
  },
  {
    "accountNumber": "7234542316",
    "accountName": "IGUH WIDIPANGESTU",
    "desc": "BSI TAB HAJI INDONESIA MUDHARABAH",
    "currency": "IDR",
    "category": "6012",
    "ammountAutoSave": 0,
    "registerStatus": "N"
  }
]
```

- Response Negative :

```json
{
  "responseCode": "01",
  "responseMessage": "Failed",
  "errorCode": "EMS-99-500",
  "errorMessage": "Not Found"
}
```


## Get History Transaction berdasarkan ID Registration

```bash
curl --request GET \
 --url 'http://10.0.118.39:5556/gw-autoemasapi/v1/inquiry/getHistoryTransactionByIdRegistration?idRegistration=15a2de5b-1dcc-4882-a90dddca8b04e0c8' \
 --header 'Authorization: Bearer 
eyJraWQiOiJzc29zIiwiYWxnIjoiUlM1MTIifQ.eyJzdWIiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS0
5MTIwYmY2MTQ0NzEiLCJhdWQiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS05MTIwYmY2MTQ
0NzEiLCJhcHBJZCI6IjUyNWIzYTYxLTg5NjgtNDc5ZC05YTQ1LTkxMjBiZjYxNDQ3MSIsImlzcyI6IkFQS
UdXIiwiZXhwIjoxNjk0Njg4NjI0LCJpYXQiOjE2OTQ2NTg2MjR9.g4BMsZ7eUk75cW57xmBoUtzQsgSi-HinY7wrCBIm-322H7b53VQW9HQAdOY9bGxU3Pn_6vgTp0uNcxN9O10-
lUK2YwLtfehZ0w-Gn6qc2uifsBDHgKKVCZvo4ansJ7RURB1ZY_avCEO6eaExcPhf-2RPE3HNAtz48MykrDA_1BkqR9cjQZU0bcVdVLNwYHnZg8bsRtAs5p8hENsU5hS1cQu9kJxQrGzN2Gi0
5eoFf9XbLepgqHUEIBICiB310eBKYzS-CFD2mF7nQIB6eOISfDDR0-3onR8fdlDRVq3oKObDS_0Lb7lQ4XkiWthpz1FlpWfLbYnMl4QBVeqw_hA' \
 --header 'User-Agent: insomnia/2023.5.8'

```
- Request : Tidak ada request body

- Response Positive :

```json
[
  {
    "id": "string",
    "rekeningEmas": "string",
    "idRegistration": "string",
    "prosentasePajak": "string",
    "beratEmas": "string",
    "ftcbs": "string",
    "totalNominalTransaksi": "string",
    "pph": "string",
    "refferenceNumber": "string",
    "rrni": "string",
    "status": "string",
    "nominalTransaksi": "string",
    "createdAt": "2023-09-07T08:14:26.690Z",
    "remark": "string"
  }
]
```
- Response Negative
```json
{
  "responseCode": "01",
  "responseMessage": "Failed",
  "errorCode": "EMS-99-404",
  "errorMessage": "Not Found"
}
```

## Get History Transaction berdasarkan Rekening Emas

```bash
curl --request GET \
 --url 'http://10.0.118.39:5556/gw-autoemasapi/v1/inquiry/getHistoryTransactionByRekeningEmas?rekeningEmas=' \
 --header 'Authorization: Bearer 
eyJraWQiOiJzc29zIiwiYWxnIjoiUlM1MTIifQ.eyJzdWIiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS0
5MTIwYmY2MTQ0NzEiLCJhdWQiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS05MTIwYmY2MTQ
0NzEiLCJhcHBJZCI6IjUyNWIzYTYxLTg5NjgtNDc5ZC05YTQ1LTkxMjBiZjYxNDQ3MSIsImlzcyI6IkFQS
UdXIiwiZXhwIjoxNjk0Njg4NjI0LCJpYXQiOjE2OTQ2NTg2MjR9.g4BMsZ7eUk75cW57xmBoUtzQsgSi-HinY7wrCBIm-322H7b53VQW9HQAdOY9bGxU3Pn_6vgTp0uNcxN9O10-
lUK2YwLtfehZ0w-Gn6qc2uifsBDHgKKVCZvo4ansJ7RURB1ZY_avCEO6eaExcPhf-2RPE3HNAtz48MykrDA_1BkqR9cjQZU0bcVdVLNwYHnZg8bsRtAs5p8hENsU5hS1cQu9kJxQrGzN2Gi0
5eoFf9XbLepgqHUEIBICiB310eBKYzS-CFD2mF7nQIB6eOISfDDR0-3onR8fdlDRVq3oKObDS_0Lb7lQ4XkiWthpz1FlpWfLbYnMl4QBVeqw_hA' \
 --header 'User-Agent: insomnia/2023.5.8'
```

- Request : tidak ada request body

- Response Positive : 

```json
[
  {
    "id": "string",
    "rekeningEmas": "string",
    "idRegistration": "string",
    "prosentasePajak": "string",
    "beratEmas": "string",
    "ftcbs": "string",
    "totalNominalTransaksi": "string",
    "pph": "string",
    "refferenceNumber": "string",
    "rrni": "string",
    "status": "string",
    "nominalTransaksi": "string",
    "createdAt": "2023-09-07T08:11:18.639Z",
    "remark": "string"
  }
]
```

- Response Negative :
```json
{
  "responseCode": "01",
  "responseMessage": "Failed",
  "errorCode": "EMS-99-404",
  "errorMessage": "Not Found"
}
```

## Get Auto Emas Portfolio berdasarkan Rekening Emas

```bash
curl --request GET \
 --url 'http://10.0.118.39:5556/gw-autoemasapi/v1/inquiry/getAutoEmasPortofolio?rekeningEMas=7001305338' \
 --header 'Authorization: Bearer 
eyJraWQiOiJzc29zIiwiYWxnIjoiUlM1MTIifQ.eyJzdWIiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS0
5MTIwYmY2MTQ0NzEiLCJhdWQiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS05MTIwYmY2MTQ
0NzEiLCJhcHBJZCI6IjUyNWIzYTYxLTg5NjgtNDc5ZC05YTQ1LTkxMjBiZjYxNDQ3MSIsImlzcyI6IkFQS
UdXIiwiZXhwIjoxNjk0Njg4NjI0LCJpYXQiOjE2OTQ2NTg2MjR9.g4BMsZ7eUk75cW57xmBoUtzQsgSi-HinY7wrCBIm-322H7b53VQW9HQAdOY9bGxU3Pn_6vgTp0uNcxN9O10-
lUK2YwLtfehZ0w-Gn6qc2uifsBDHgKKVCZvo4ansJ7RURB1ZY_avCEO6eaExcPhf-2RPE3HNAtz48MykrDA_1BkqR9cjQZU0bcVdVLNwYHnZg8bsRtAs5p8hENsU5hS1cQu9kJxQrGzN2Gi0
5eoFf9XbLepgqHUEIBICiB310eBKYzS-CFD2mF7nQIB6eOISfDDR0-3onR8fdlDRVq3oKObDS_0Lb7lQ4XkiWthpz1FlpWfLbYnMl4QBVeqw_hA' \
 --header 'User-Agent: insomnia/2023.5.8'
```

- Request : Tidak ada request body nya

- Response Positive : 
```json
[
  {
    "idRegistration": "15a2de5b-1dcc-4882-a90d-ddca8b04e0c8",
    "rekeningDebit": "7234537894",
    "type": "BGH"
  },
  {
    "idRegistration": "25301f55-32d2-40c5-ac82-9517f3b91417",
    "rekeningDebit": "7001305338",
    "type": "TAB"
  }

]
```

- Response Negative :

```json
{
  "responseCode": "01",
  "responseMessage": "Failed",
  "errorCode": "EMS-99-404",
  "errorMessage": "Not Found"
}
```

## Get Registration Data berdasarkan ID Registration

```bash
curl --request GET \
 --url 'http://10.0.118.39:5556/gw-autoemasapi/v1/inquiry/getRegistrationData?idRegistration=15a2de5b-1dcc-4882-a90d-ddca8b04e0c8' \
 --header 'Authorization: Bearer 
eyJraWQiOiJzc29zIiwiYWxnIjoiUlM1MTIifQ.eyJzdWIiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS0
5MTIwYmY2MTQ0NzEiLCJhdWQiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS05MTIwYmY2MTQ
0NzEiLCJhcHBJZCI6IjUyNWIzYTYxLTg5NjgtNDc5ZC05YTQ1LTkxMjBiZjYxNDQ3MSIsImlzcyI6IkFQS
UdXIiwiZXhwIjoxNjk0Njg4NjI0LCJpYXQiOjE2OTQ2NTg2MjR9.g4BMsZ7eUk75cW57xmBoUtzQsgSi-HinY7wrCBIm-322H7b53VQW9HQAdOY9bGxU3Pn_6vgTp0uNcxN9O10-
lUK2YwLtfehZ0w-Gn6qc2uifsBDHgKKVCZvo4ansJ7RURB1ZY_avCEO6eaExcPhf-2RPE3HNAtz48MykrDA_1BkqR9cjQZU0bcVdVLNwYHnZg8bsRtAs5p8hENsU5hS1cQu9kJxQrGzN2Gi0
5eoFf9XbLepgqHUEIBICiB310eBKYzS-CFD2mF7nQIB6eOISfDDR0-3onR8fdlDRVq3oKObDS_0Lb7lQ4XkiWthpz1FlpWfLbYnMl4QBVeqw_hA' \
 --header 'User-Agent: insomnia/2023.5.8'
```

- Request : Tidak ada request body

- Response Positive : 

```json
{
  "idRegistration": "15a2de5b-1dcc-4882-a90d-ddca8b04e0c8",
  "noRekeningEmas": "7001305399",
  "nama": "IGUH WIDIPANGESTU",
  "noRekeningDebit": "7234537894",
  "channel": "MBG",
  "active": true,
  "tanggalBerhenti": "2025-02",
  "type": "BGH"
}
```

- Response Negative :

```json
{
  "responseCode": "01",
  "responseMessage": "Failed",
  "errorCode": "EMS-99-404",
  "errorMessage": "Not Found"
}
```

## Get Auto Save Emas Data by CIF

```bash
curl --request GET \
 --url 'http://10.0.118.39:5556/gw-autoemas-api/v1/inquiry/getAutoSaveEmasData?cif=73005846' 
\
 --header 'Authorization: Bearer 
eyJraWQiOiJzc29zIiwiYWxnIjoiUlM1MTIifQ.eyJzdWIiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS0
5MTIwYmY2MTQ0NzEiLCJhdWQiOiI1MjViM2E2MS04OTY4LTQ3OWQtOWE0NS05MTIwYmY2MTQ
0NzEiLCJhcHBJZCI6IjUyNWIzYTYxLTg5NjgtNDc5ZC05YTQ1LTkxMjBiZjYxNDQ3MSIsImlzcyI6IkFQS
UdXIiwiZXhwIjoxNjk0Njg4NjI0LCJpYXQiOjE2OTQ2NTg2MjR9.g4BMsZ7eUk75cW57xmBoUtzQsgSi-HinY7wrCBIm-322H7b53VQW9HQAdOY9bGxU3Pn_6vgTp0uNcxN9O10-
lUK2YwLtfehZ0w-Gn6qc2uifsBDHgKKVCZvo4ansJ7RURB1ZY_avCEO6eaExcPhf-2RPE3HNAtz48MykrDA_1BkqR9cjQZU0bcVdVLNwYHnZg8bsRtAs5p8hENsU5hS1cQu9kJxQrGzN2Gi0
5eoFf9XbLepgqHUEIBICiB310eBKYzS-CFD2mF7nQIB6eOISfDDR0-3onR8fdlDRVq3oKObDS_0Lb7lQ4XkiWthpz1FlpWfLbYnMl4QBVeqw_hA' \
 --header 'User-Agent: insomnia/2023.5.8'
```

- Request : Tidak ada request body

- Response Positive :

```json
[
  {
    "type": "2 - BAGI HASIL",
    "data": []
  },
  {
    "type": "1 - TABUNGAN",
    "data": []
  }
]
```

- Response Negative :

```json
{
  "responseCode": "01",
  "responseMessage": "Failed",
  "errorCode": "EMS-99-404",
  "errorMessage": "Not Found"
}
```