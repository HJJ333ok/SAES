# SAES
SAES

基础界面

![1](https://github.com/HJJ333ok/SAES/assets/129488158/63f39a78-0578-4916-b875-a2ff04fca2e4)


 第1关：基本测试       
 根据S-AES算法编写和调试程序，提供GUI解密支持用户交互。输入可以是16bit的数据和16bit的密钥，输出是16bit的密文。
 
![2](https://github.com/HJJ333ok/SAES/assets/129488158/c60010fa-baea-4bc6-b3cf-4e320289d65d)

 第2关：交叉测试考虑到是"算法标准"，所有人在编写程序的时候需要使用相同算法流程和转换单元(替换盒、列混淆矩阵等)，以保证算法和程序在异构的系统或平台上都可以正常运行。设有A和B两组位同学(选择相同的密钥K)；则A、B组同学编写的程序对明文P进行加密得到相同的密文C；或者B组同学接收到A组程序加密的密文C，使用B组程序进行解密可得到与A相同的P。

通过与其他小组的交叉测试可以得到正确的明文（由于代码存在一些未知bug，在ui界面无法显示正确数据，改为在控制台显示）

![3](https://github.com/HJJ333ok/SAES/assets/129488158/c6e74fe0-ce27-4b3c-8232-6a6500bbbff6)

![3 1](https://github.com/HJJ333ok/SAES/assets/129488158/628e0621-b456-4519-8443-53f8d6d4cc19)

第3关：扩展功能考虑到向实用性扩展，加密算法的数据输入可以是ASII编码字符串(分组为2 Bytes)，对应地输出也可以是ACII字符串(很可能是乱码)。

对于ASCII码的输入

![4](https://github.com/HJJ333ok/SAES/assets/129488158/ae7d7103-1062-4e1d-a5d2-27744defc5f9)

3.4 第4关：多重加密

3.4.1 双重加密将S-AES算法通过双重加密进行扩展，分组长度仍然是16 bits，但密钥长度为32 bits。

对代码进行拓展，使密钥长度为32bit，得出结果如下

![BCNQVW8RG73Z( 0AG8BVG95](https://github.com/HJJ333ok/SAES/assets/129488158/e9e7ad12-0497-4f5a-9b80-29d6203ead44)
![(5BA33SD_{FO0BPK1SYDVPJ](https://github.com/HJJ333ok/SAES/assets/129488158/464f4cd0-b74b-467b-8da7-2ceb2aaaffe4)


3.4.2 中间相遇攻击假设你找到了使用相同密钥的明、密文对(一个或多个)，请尝试使用中间相遇攻击的方法找到正确的密钥Key(K1+K2)。


3.4.3 三重加密将S-AES算法通过三重加密进行扩展，下面两种模式选择一种完成：(1)按照32 bits密钥Key(K1+K2)的模式进行三重加密解密，(2)使用48bits(K1+K2+K3)的模式进行三重加解密。

选择模式一进行三重加密

![(G8_)YDXDY639S 78%_}MXC](https://github.com/HJJ333ok/SAES/assets/129488158/9ff75f94-bc0e-4825-8c0c-2f1c2414efcb)

