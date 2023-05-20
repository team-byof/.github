## Bring Your Own Face
![BYOF_LOGO](https://github.com/glitch-hackathon-2023/.github/assets/63194399/70c669e2-8e0c-4545-b688-616cb1367e09)

### overview
* Bring Your Own Face, or BYOF, is a trustless and seamless solution with ZK face ID and Account Abstraction.
* With BYOF, users only need their faces to manage their keys and send transactions.

### Problems
1. UX is one of the most severe problems that block the mass adoption of web3. 
2. Think of a wallet, you must manage your seed phrase, and go through several steps to use dApps such as connect wallet.
3. One meaningful solution could be account abstraction with biometric authentication. Think of how you send money in web2. You just click the bank app on your phone, verify your bio auth, and done! 
4. However, it relies on Apple, Samsung, or Google. It revives the third-party issue which breaks the core value of web3: trustless.

### Solution
* We suggest an AA integration with ZK proof of bio-auth. With this solution, we eventually get seamless UX in a trustless way.  
  
### Products
##### Userflow
<img width="422" alt="스크린샷 2023-05-20 오후 9 37 18" src="https://github.com/glitch-hackathon-2023/.github/assets/63194399/645529e3-bc23-4af7-bb94-44d2aff103c0">

1. Alice creates an account with her face authentication, and deploys AA contract containing ZK verification.
2. Let’s say Alice wants to swap tokens in Uniswap. All she needs to do is just verifying her face and submitting ZK proof.

### Architecture
<img width="341" alt="스크린샷 2023-05-21 오전 12 09 46" src="https://github.com/glitch-hackathon-2023/.github/assets/63194399/69fc052e-ca18-4510-93c3-342c48306ec3">

1. If face ID data, or feature vectors is in the acceptable error ratio, fuzzy commitment scheme can recover the original commitment.
2. It means that if you are the same person with the original key owner, you can make the same commitment value. 
3. And then ZK comes in. Here, ZK is used to conceal the critical privacy data such as face feature vectors and ensure that calculation is correct.
4. So in conclusion, you can check whether it’s the same person by commitment which is public input without revealing the original data thanks to ZK proof.
  
#### Vision and Roadmap
* We provide ZK Face ID plus AA integration as an SDK. Anyone can build their own dApps or products. Also, we will support Polygon ZK Id for this SDK, which helps developers build human-verified anonymous communities or dApps such as ZK Among Us. 

