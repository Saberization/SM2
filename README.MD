# SM2 国密前端加密代码

**经过测试，同一密钥对同一数据进行 `50万` 次加密，后端解密一切正常**

## 依赖资源

- `crypto-js`

## 使用方法

### 加密：

```js
const msg = 'hello world'
const pubkeyHex = '0452712EBA7FE2C9615F6DE59C6EF662R085BD52B25952597CC95014BB8F201987F8D818EFFE710DBEC08FE2E4C7E3E0113EEBAB4B0E8B044E1A3CC8B149D76BE7';
const cipherMode = 0;

// 获取加密过后的密文
const result = sm2Encrypt(msg, pubkeyHex, cipherMode);
```

| 参数 | 参数类型 | 说明 |
| ---- | ---- | ---- |
| msg | String | 加密的文本 |
| pubkeyHex | String | 公钥 hex |
| cipherMode | String | 0: C1C2C3、1: C1C3C2 |