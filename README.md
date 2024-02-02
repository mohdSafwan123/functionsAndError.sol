Loan System Smart Contract

This smart contract, named LoanSystem, facilitates a simple loan system between a creditor and debtors on the Ethereum blockchain. It is designed to be used with Solidity version 0.6.12 up to, but not including, version 0.9.0. The contract operates with a set of simulated balances and a transaction fee.
Table of Contents

   . Contract Overview
   . Functions
   . Modifiers
   . Usage
   . License

# Contract Overview
## Variables

    creditor: Ethereum address of the creditor.
    creditorBalance: Simulated balance of the creditor in wei.
    debtorBalances: Array representing simulated balances of debtors in wei.
    transactionFee: Simulated transaction fee in wei.
    isDebtorOnCooldown: Array of boolean values indicating whether a debtor is on cooldown.

## Modifiers

    onlyCreditor: Restricts access to functions only to the creditor.

## Functions

    getCreditorBalance(): Retrieve the balance of the creditor.
    getDebtorBalance(uint _debtorId): Retrieve the balance of a specified debtor.
    sendLoan(uint _loanAmount, uint _debtorId): Initiate a loan transaction from the creditor to a specified debtor.
    debtorCooldownStatus(uint _debtorId): Check if a debtor is currently on cooldown.
    resetDebtorCooldown(uint _debtorId): Reset the cooldown status of a debtor.
    updateTransactionFee(): Increase the transaction fee by 1 wei.
    viewTransactionFee(): Retrieve the current transaction fee.
    resetTransactionFee(): Reset the transaction fee to its initial value.

# Functions
1. getCreditorBalance()

    Description: Retrieve the balance of the creditor.
    Access: Only accessible by the creditor.

2. getDebtorBalance(uint _debtorId)

    Description: Retrieve the balance of a specified debtor.
    Parameters:
        _debtorId: ID of the debtor (0 or 1).
    Access: Only accessible by the creditor.

3. sendLoan(uint _loanAmount, uint _debtorId)

    Description: Initiate a loan transaction from the creditor to a specified debtor.
    Parameters:
        _loanAmount: Amount of the loan in wei.
        _debtorId: ID of the debtor (0 or 1).
    Access: Only accessible by the creditor.

4. debtorCooldownStatus(uint _debtorId)

    Description: Check if a debtor is currently on cooldown.
    Parameters:
        _debtorId: ID of the debtor (0 or 1).
    Access: Only accessible by the creditor.
    Returns: Boolean indicating cooldown status.

5. resetDebtorCooldown(uint _debtorId)

    Description: Reset the cooldown status of a debtor.
    Parameters:
        _debtorId: ID of the debtor (0 or 1).
    Access: Only accessible by the creditor.

6. updateTransactionFee()

    Description: Increase the transaction fee by 1 wei.
    Access: Only accessible by the creditor.

7. viewTransactionFee()

    Description: Retrieve the current transaction fee.
    Access: Only accessible by the creditor.
    Returns: Current transaction fee.

8. resetTransactionFee()

    Description: Reset the transaction fee to its initial value.
    Access: Only accessible by the creditor.

# Usage

    Deploy the LoanSystem contract to the Ethereum blockchain.
    Set the initial balances and transaction fee.
    Access various functions to interact with the loan system.
