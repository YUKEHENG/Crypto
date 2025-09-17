# Crypto学习笔记

## 密码学

cryptographic hash function:
- cllision resistance（抗碰撞性，即没有一个好的办法人为制造哈希碰撞）->不可篡改。这个理论无法被证明
- hiding(哈希函数计算不可逆）除非遍历
  实现digital commitment,实现的时候可以拼接一个随机数来哈希，避免输入空间不够大的情况。

  挖矿就是找到一个随机数，与区块头一起算哈希值小于困难值。只能遍历。
  不容易挖但是容易验证

  创户：
  在本地得到一个（公钥、私钥）对。
  用公钥加密，用私钥解密。想传递信息，用对方公钥加密，对方用自己的私钥解密。
  非对称加密体系
  签名用公钥，验证签名用私钥


  ## 数据结构
  hash pointers保存起始地址和哈希值。无论哪个地方被篡改，最后的哈希值都会被改变。
  Merkle tree 由data blocks和hash pointers构成。只需记录root hash。用来提供Merkle proof用来证明某个交易是否被写入区块链
  
