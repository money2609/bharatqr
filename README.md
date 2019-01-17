# bharatqr

BharatQr Api's

1) Registration Api  

``Request``  
curl -X POST \
  https://testqr.wibmopay.com/qr/merchant/register \
  -H 'content-type: multipart/form-data; \
  -F 'merchant_display_name=Faiz Javed' \
  -F merchant_mobile=7829153006 \
  -F merchant_email=faiz.javed@wibmo.com \
  -F merchant_name=apu4-p2m \
  -F checksum=99671A1996B84BB908F4608DF11E5CFFFB05E64ECD786F86CD1BD13924C9BED884C4E42A4BD7837D5973942BAE9CCA25E48341683FEF7FE4D898CAE8C7F67658

``checksum creation params``  
merchant_display_name|merchant_mobile|merchant_email|merchant_name|merchant_secret


``Response``  

status code 200

{
"status": "success", 
"status_code": 200,
"response": {
	"message":"Merchant Registerred successfully",
	"wallet_id":"15070"	
},
"code": "E200"}

status code 400

{
"status": "error", 
"status_code": 400,
"response": {
	"message":"Bharat QR Not Enabled",
	"wallet_id":""	
},
"code": "E129"}


status code 403

{
"status": "error", 
"status_code": 403,
"response": {
	"message":"Forbidden, Invalid Cheksum",
	"wallet_id":""	
},
"code": "E127"}

