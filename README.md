# Joint Savings Smart Contract

<img src="https://github.com/Nievz/Joint_Saving_Accounts/blob/main/Images/20-5-challenge-image.png" alt="Logo" width="1000" height="450">

Welcome to the Joint Savings Smart Contract GitHub repository. This project presents the deployment of a Solidity smart contract named `JointSavings` designed to automate the management of joint savings accounts on an Ethereum-compatible blockchain.

## Overview

The primary goal of this smart contract is to enable two users to jointly control a savings account, facilitating shared financial resource management. It offers functionalities such as depositing and withdrawing funds, providing a secure and transparent way to manage shared financial assets.

## Smart Contract Features

### Initialization

- Two `address payable` variables, `accountOne` and `accountTwo`, represent the joint account holders.
- An `address public` variable, `lastToWithdraw`, tracks the last user to make a withdrawal.
- Two `uint public` variables, `lastWithdrawAmount` and `contractBalance`, store information about the last withdrawal amount and the current contract balance.

### Withdrawal Functionality

- The `withdraw` function allows users to make withdrawals from the joint account.
- It verifies that the recipient of the withdrawal is either `accountOne` or `accountTwo`, ensuring ownership.
- A balance check ensures that the contract holds sufficient funds for the withdrawal.
- The function records the last withdrawal details, including the recipient and amount.
- After a successful withdrawal, the contract balance is updated.

### Deposit Functionality

- The `deposit` function allows users to deposit funds into the joint account.
- It updates the contract balance to reflect the new total balance after the deposit.

### Account Management

- The `setAccounts` function allows the assignment of authorized Ethereum addresses to `accountOne` and `accountTwo`. This function is essential for determining joint account ownership.

## Usage

### Deployment

To deploy the `JointSavings` smart contract, we followed these steps:

1. Compile the smart contract code without any compilation errors.

2. Use the Remix IDE's "Deploy & Run Transactions" panel, selecting "Remix Shanghai VM" as the execution environment.

3. Click the "Deploy" button to initiate the contract deployment. Confirm that the deployment process completes successfully.

### Interacting with the Contract

After deploying the contract, users can interact with it as follows:

1. Use the `setAccounts` function to define the authorized Ethereum addresses that can withdraw funds from the contract. users can generate dummy addresses using the [Vanity-ETH](#) website or use the provided Ethereum addresses.

   - Dummy account1 address: `0x0c0669Cd5e60a6F4b8ce437E4a4A007093D368Cb`
   - Dummy account2 address: `0x7A1f3dFAa0a4a19844B606CD6e91d693083B12c0`

2. Test the deposit functionality by sending various amounts of Ether to the contract. After each transaction, we verify the updated contract balance using the `contractBalance` function.

   - Transaction 1: Send 1 Ether as wei.
   - Transaction 2: Send 10 Ether as wei.
   - Transaction 3: Send 5 Ether.

3. Validate the withdrawal functionality by making withdrawals from the contract. After each transaction, we confirmed that the funds were successfully withdrawn from the contract. Additionally, we use the `lastToWithdraw` and `lastWithdrawAmount` functions to verify the recipient and withdrawal amount.

## Execution Results

The `Execution_Results` folder contains screenshots capturing the execution of the contract during testing. These images validate the deposit and withdrawal transactions, demonstrating the successful operation of the `JointSavings` smart contract within the JavaScript VM environment.
  # Functions
<p align="center" style="display: flex;" >
  <img src="https://github.com/Nievz/Joint_Saving_Accounts/blob/main/Execution_Results/functions.png" alt="Logo" width="1000" height="400">
</p>

  # Transaction 1: Sending 1 ether as wei.
<p align="center" style="display: flex;" >
  <img src="https://github.com/Nievz/Joint_Saving_Accounts/blob/main/Execution_Results/One.png" alt="Logo" width="1000" height="400">
</p>

  # Transaction 2: Sending 10 ether as wei.
<p align="center" style="display: flex;" >
  <img src="https://github.com/Nievz/Joint_Saving_Accounts/blob/main/Execution_Results/Ten%20ether.png" alt="Logo" width="1000" height="400">
</p>

  # Transaction 3: Sending 5 ether.
<p align="center" style="display: flex;" >
  <img src="https://github.com/Nievz/Joint_Saving_Accounts/blob/main/Execution_Results/five%20ether.png" alt="Logo" width="1000" height="400">
</p>

  # Withdrawing 5 ether
<p align="center" style="display: flex;" >
  <img src="https://github.com/Nievz/Joint_Saving_Accounts/blob/main/Execution_Results/five%20withdraw.png" alt="Logo" width="1000" height="400">
</p>

  # Withdrawing 10 ether
<p align="center" style="display: flex;" >
  <img src="https://github.com/Nievz/Joint_Saving_Accounts/blob/main/Execution_Results/ten%20withdraw.png" alt="Logo" width="1000" height="400">
</p>

  # Using lastToWithdraw and lastWithdrawAmount functions to verify Transactions
<p align="center" style="display: flex;" >
  <img src="https://github.com/Nievz/Joint_Saving_Accounts/blob/main/Execution_Results/last%20to%20withdraw.png" alt="Logo" width="500" height="500">
</p>

## Conclusion
In conclusion, the JointSavings smart contract offers a robust solution for joint savings account management on an Ethereum-compatible blockchain. It demonstrates the potential of blockchain technology to streamline financial processes securely and transparently. By meeting project requirements, conducting thorough testing, and providing clear documentation, we contribute to the fintech startup's mission of disrupting the finance industry. This project showcases the transformative power of blockchain innovation in reshaping financial services and highlights the continued evolution of blockchain technology.

## License

Distributed under the MIT License. See LICENSE.txt for more information.

<!-- ACKNOWLEDGMENTS -->
## Acknowledgments
* [https://bootcampspot.instructure.com/courses/3828/assignments/57447?module_item_id=1010128]()
