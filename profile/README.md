# Ring DAO

Ring DAO is a tooling for Decentralized Autonomous Organizations (DAOs) that innovates by using ring signatures. This unique approach allows the toolkit to provide privacy to DAO members through token-gated authentication based on ring signatures.

## Key Features

- **Privacy-Preserving Authentication:** Ring DAO leverages ring signatures to enable token-gated authentication, allowing members to interact with the DAO without revealing their individual identities.
- **Secure Voting System:** The project also innovates by incorporating ring signatures into the DAO's voting system, enhancing the privacy and security of the decision-making process.
-  **Decentralized Governance:** Ring DAO is designed to empower DAO members with a decentralized governance model, where decisions are made collectively and transparently.
-  **Metamask Snap Integration:** Ring DAO leverages the Metamask Snap API to seamlessly integrate the ring signature process into the user experience, providing a familiar and secure way for members to authenticate and vote within the DAO.

## Ring Signatures 
Ring signatures are a type of digital signature that provide anonymity and privacy for the signer. The signer creates a signature using their own private key, but their identity is hidden within a "ring" of multiple public keys.

Key features of ring signatures:

- **Anonymity**: The signer's identity is obfuscated within the ring of public keys.
- **Unforgeability**: Only a member of the ring can create a valid signature.
- **Efficiency**: Ring signatures can be generated and verified efficiently.

Ring signatures have applications in areas like confidential transactions, whistleblowing, and e-voting.

For this project, we utilize [Alice's Ring LSAG TS library](https://github.com/Cypher-Laboratory/Alice-s-Ring-LSAG-TS), a TypeScript implementation of the ring signature algorithm. 

## Project Structure :

The project is composed of several key components that work together to provide a secure and privacy-preserving governance solution for decentralized autonomous organizations. 
- [**Metamask Snap**](https://github.com/ring-dao/LSAG-snap) :The Metamask Snap is a crucial part of the Ring DAO system, as it allows users to create ring signatures seamlessly while maintaining the safety and user experience provided by the Metamask wallet. This integration enables DAO members to authenticate and interact with the DAO without revealing their individual identities.
- [**WebApp**](https://github.com/ring-dao/web_app) : The Ring DAO web application, built using React, provides a user-friendly interface for DAO members to interact with each other and the DAO's governance processes. The web application leverages the ring signature functionality to anonymize the users' identities, ensuring that their participation in the DAO is kept private.
- [**Backend**](https://github.com/ring-dao/backend) : The backend component, built using Express, serves as the intermediary between the web application and the underlying database. This backend ensures secure and efficient data transfer, while also enforcing the privacy guarantees provided by the ring signature system.
To maintain the anonymity of DAO members, every interaction that requires write permission goes through a middleware that verifies a ring signature. The backend never knows which specific address is calling it, as the identity is obfuscated within the ring of public keys. 
- [**Smart-Contract**](https://github.com/ring-dao/LSAG-evm-verifier) : The Ring DAO smart contracts are deployed on Scroll, enabling DAO members to vote anonymously using ring signatures. This approach ensures that the DAO's decision-making process is transparent and secure, while preserving the privacy of the individual members.
