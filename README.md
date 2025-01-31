### README for ErrorHandling Project

---

#### **Project Title**
ErrorHandling Solidity Smart Contract

#### **Description**
`ErrorHandling` is a Solidity smart contract that demonstrates different error handling mechanisms in Solidity, including `require`, `revert`, and `assert`. The contract includes functions to validate numbers, addresses, and differences between numbers, providing practical examples of how each error handling mechanism operates.

---

#### **Getting Started**

##### **Installing**

1. **Clone the Repository:**
   ```sh
   git clone https://github.com/ZPiya/ErrorHandling.git
   cd ErrorHandling
   ```

2. **Install Dependencies:**
   Ensure you have [Node.js](https://nodejs.org/) and [npm](https://www.npmjs.com/) installed. Then install Truffle if you plan to use it for development:
   ```sh
   npm install -g truffle
   ```

##### **Executing Program**

1. **Open Remix IDE:**
   - Go to [Remix Ethereum IDE](https://remix.ethereum.org/).
   - Create a new file named `ErrorHandling.sol` and paste the contract code from the repository.

2. **Compile the Contract:**
   - In the Remix IDE, select the `ErrorHandling.sol` file.
   - Go to the "Solidity Compiler" tab and click "Compile ErrorHandling.sol".

3. **Deploy the Contract:**
   - Go to the "Deploy & Run Transactions" tab.
   - Ensure the environment is set to "JavaScript VM (London)".
   - Click "Deploy".

4. **Interact with the Contract:**
   - After deployment, the contract functions will appear in the "Deployed Contracts" section.
   - You can interact with functions like `checkEvenNumber`, `validateAddress`, and `verifyDifference` directly from the Remix interface.

   Example interactions:
   ```javascript
   // Check if the number is even and within the specified range
   await instance.checkEvenNumber(44); // This will pass
   await instance.checkEvenNumber(101); // This will fail with revert error
   await instance.checkEvenNumber(42); // This will fail with assert error

   // Validate the address
   await instance.validateAddress("0x0000000000000000000000000000000000000000"); // This will fail with require error
   await instance.validateAddress("0x1234567890123456789012345678901234567890"); // This will fail with revert error
   await instance.validateAddress("0x2222222222222222222222222222222222222222"); // This will pass

   // Verify the difference between two numbers
   let result = await instance.verifyDifference(30, 10); // This will pass
   result = await instance.verifyDifference(100, 30); // This will fail with revert error
   result = await instance.verifyDifference(50, 50); // This will fail with assert error
   ```

##### **Help**
For common issues, ensure you have the correct versions of dependencies and the correct settings in the Remix IDE.

If you encounter issues:
- Check the Remix IDE documentation for setup and usage.
- Consult the [Solidity documentation](https://docs.soliditylang.org/) for details on `require`, `revert`, and `assert`.

For additional support, you can raise an issue on the project repository or seek help in Solidity or Ethereum development forums.

---

#### **Authors**

- **Zuphia Rosal**
  - Email: 202111617@fit.edu.ph

---

#### **License**
This project is licensed under the MIT License - see the LICENSE.md file for details.

---

Feel free to reach out if you have any questions or need further assistance!
