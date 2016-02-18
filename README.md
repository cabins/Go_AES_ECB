# Go语言 AES ECB模式加解密

AES的ECB模式被认为是不安全的，所以Go语言没有提供官方函数，这里使用Go语言库中的块加解密算法，实现了AES的ECB模式加密和解密算法，以及PKCS7Pad补全算法。

## 安装

```go
go get github.com/cabins/Go_AES_ECB
```

## 使用

```go
import (
	"github.com/cabins/Go_AES_ECB"
)

func main() {
	key := "thisiskeyandlen>16"
	//加密
	ciphertext := security.Encrypt(security.PKCS7Pad([]byte("asdasdasdasdasd")), key)
	//解密
	plaintext := string(security.PKCS7UPad([]byte(security.Decrypt(ciphertext, key))))
}
```
