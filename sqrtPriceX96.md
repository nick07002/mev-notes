ref: https://youtu.be/EV23xTgWsnY

- The sqrtPriceX96 value in Uniswap V3 Pools represents the ratio between the two tokens in the pool. Its data type in the pool contract is an unsigned integer 160, intended to be a binary fixed point number, where 64 bits of the 160 bits represent the integer portion and the remaining 96 bits represent the decimal portion.
- The sqrtPriceX96 value is a binary value of the format q64.96. It can be converted from its base 10 form to base 2 form by calling toString on the number and passing in 2. This makes the value readable in binary form.
- To convert sqrtPriceX96 to a human-readable ratio, it is first squared (multiplied by itself), which gives a ratio x 192, as squaring the square root of a number gives the original number and squaring x96 gives x192 (96+96 equals 192).
- Next, to get the human-readable ratio, the squared sqrtPriceX96 (ratio x192) is divided by 2 to the power of 192. This operation shifts the integer portion of the number one place to the right, similar to how division by 10 shifts the integer portion of a base-10 number one place to the right.
- With the example provided in the transcript, the resulting human-readable ratio (0.004353) is the ratio between Uniswap token and wrapped ether in the Uniswap app. If one wants to find the ratio the other way around (from wrapped ether to Uniswap), it's as simple as inverting the obtained ratio.

- Uniswap V3 Pools中的sqrtPriceX96值代表池中两种代币的比率。在池合约中，其数据类型为无符号整数160，这意味着它应被视为二进制固定点数，其中160位中的64位表示整数部分，剩下的96位表示小数部分。
- sqrtPriceX96值是格式为q64.96的二进制值。通过对该数调用toString并传入2，可以将其从基数10形式转换为基数2形式。这使得该值以二进制形式可读。
- 要将sqrtPriceX96转换为人类可读的比率，首先对其进行平方（自乘），得到比率x192，因为对一个数的平方根进行平方操作将得到原始数值，同时对x96进行平方将得到x192（96+96等于192）。
- 接下来，为了得到人类可读的比率，将平方后的sqrtPriceX96（即比率x192）除以2的192次方。这个操作将该数的整数部分向右移动一位，类似于10进制数除以10将整数部分向右移动一位的操作。
- 根据对话稿中提供的例子，得到的人类可读的比率（0.004353）是Uniswap代币和wrapped ether在Uniswap应用中的比率。如果想要找出反过来（从wrapped ether到Uniswap）的比率，只需取得到的比率的倒数即可。
