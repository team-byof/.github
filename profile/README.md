## Bring Your Own Face
![BYOF_LOGO](https://github.com/glitch-hackathon-2023/.github/assets/63194399/70c669e2-8e0c-4545-b688-616cb1367e09)

### overview
* Bring Your Own Face, or BYOF, is a trustless and seamless solution with ZK face ID and Account Abstraction.
* With BYOF, users only need their faces to manage their keys and send transactions.

### Problems
- Low UX is one of the biggest factors blocking the mass adoption of Web3. Especially wallets should have exceptional UX, considering they often serve as the first entry point for most people into the Web3 ecosystem.
- Unfortunately, traditional wallets failed to achieve this gaol. Seed phrases are difficult to manage, and when you want to interact with dApps, you should go through multiple steps, such as wallet connect.
- On the other hand, it is easy to complete transactions simply by using fingerprint or facial recognition in web2.
- EIP-4337, also called Account Abstraction, suggests a way to bring the seamless UX of web2.
- By using Account Abstraction (AA), the number of steps required to integrate with dApps can be impressed in one step, and wallet recovery can be made easier with biometric authentication.
- The problem is that it relies on Android or Apple for biometric authentication.
- Therefore, this compromises the goal of blockchain, which is to eliminate the need for third-party intermediaries.
- Is there a way to enjoy both the benefits of improved UX through AA and enhanced security through biometric authentication?
- We suggest a ZK as a solution to achieve seamless UX by AA and security by biometric authentication in a trustless way.

### Products
##### Architecture
<img width="422" alt="스크린샷 2023-05-20 오후 9 37 18" src="https://github.com/glitch-hackathon-2023/.github/assets/63194399/645529e3-bc23-4af7-bb94-44d2aff103c0">

- User generates facial recognition data (feature vectors) with their mobile phone and uses it as a private key to create an account.
- Subsequently, the AA contract, which includes the ZK Verification contract for facial recognition, is deployed. (the service provider will pay a gas fee)
- Now, the user can perform two functions with facial recognition. The first is wallet recovery, and the second is interacting with dApps solely through facial recognition.
- To recover the wallet, the user must take facial recognition once again. After the user re-extracts facial recognition data through their mobile device, they adjust the error using the properties of fuzzy commitment to recover the facial recognition data used to generate the private key. Suppose the original feature vectors and the new feature vectors have a very low error (indicating the same person). In that case, the original value can be found through re-computation using a random value of fuzzy commitment.
- Let's consider sending a swap contract on Uniswap. You need to take facial recognition again. It will use the fuzzy commitment scheme with the new facial recognition data (feature vectors) to recover the original data. If there is no recovery error, a ZK proof is generated, stating that the recovery operation has been correctly performed and the result is true. The ZK proof is then submitted to the AA contract. Once the contractor completes the verification, it can securely send transactions on behalf of the user, replacing the need for the user's private key.

#### Vision and Roadmap
* We provide ZK Face ID plus AA integration as an SDK. Anyone can build their own dApps or products. Also, we will support Polygon ZK Id for this SDK, which helps developers build human-verified anonymous communities or dApps such as ZK Among Us. 

