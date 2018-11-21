# bharatqr

BharatQr Api's

1) Registration Api

Request
curl -X POST \
  https://testqr.wibmopay.com/qr/merchant/register \
  -H 'content-type: multipart/form-data; \
  -F 'merchant_display_name=Faiz Javed' \
  -F merchant_mobile=7829153006 \
  -F merchant_email=faiz.javed@wibmo.com \
  -F merchant_name=apu4-p2m \
  -F checksum=99671A1996B84BB908F4608DF11E5CFFFB05E64ECD786F86CD1BD13924C9BED884C4E42A4BD7837D5973942BAE9CCA25E48341683FEF7FE4D898CAE8C7F67658

checksum creation params
merchant_display_name|merchant_mobile|merchant_email|merchant_name|merchant_secret


Response

status code - 200
{
    "response": {
        "message": "Merchant registered succesfully",
        "walletId": "15070"
    },
    "status": "success"
}

status code - 403
{
    "response": {
        "message": "Merchant Forbidden",
        "walletId": ""
    },
    "status": "failed"
}

status code - 400
{
    "response": {
        "message": "Merchant Already Registered",
        "walletId": ""
    },
    "status": "failed"
}

