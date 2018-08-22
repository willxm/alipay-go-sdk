# alipay-go-sdk
支付宝支付 新版 go sdk

### usage
```
vim tools/config.go
```

```
const (
	APPID      = "your app id"
	NOTIFY_URL = "your alipay callback notify url"
)

var PRIVATE_KEY = []byte(`
-----BEGIN RSA PRIVATE KEY-----
your private key
-----END RSA PRIVATE KEY-----
`)

var PUBILC_KEY = []byte(`
-----BEGIN RSA PUBLIC KEY-----
alipay public key
-----END RSA PUBLIC KEY-----
`)

```

input your config information

```golang
  	outTradeNo := "creat your out trade no"
	charge := new(pay.Charge)
	charge.MoneyFee = totalFee
	charge.Describe = "describe"
	charge.TradeNum = outTradeNo
	reqStr := pay.Pay(charge)
```
then return reqStr to client
