
# Create Fungible Token on Aptos

## Overview

This project provides a Move module for creating and managing a fungible token on the Aptos blockchain. It allows token minting, burning, transferring, freezing, and unfreezing accounts.

## Features

-   **Token Initialization**: Create and initialize a fungible token with a name, symbol, decimals, and metadata.
    
-   **Minting**: Generate new tokens and deposit them into an account.
    
-   **Transferring**: Send tokens from one account to another.
    
-   **Burning**: Remove tokens from circulation.
    
-   **Freezing/Unfreezing**: Restrict or restore an account's ability to transfer or receive tokens.
    

## Token Details

-   **Name**: META Coin
    
-   **Symbol**: META
    
-   **Decimals**: 8
    
-   **Icon**: [META Coin Icon](https://drive.google.com/file/d/1vFm-kF6O3onxPgFJ_rVLh9YGFT_fFWM6/view?usp=sharing)
    
-   **Project URL**: [MetaSchool](http://metaschool.so)
    

## Prerequisites

-   Aptos CLI
    
-   Move CLI
    
-   Aptos Devnet/Testnet account
    

## Installation

1.  Clone the repository:
    
    ```
    git clone https://github.com/khoa93900/create-fungible-token-on-aptos.git
    cd create-fungible-token-on-aptos
    ```
    
2.  Compile the Move module:
    
    ```
    aptos move compile
    ```
    
3.  Deploy the module to Aptos:
    
    ```
    aptos move publish --profile default
    ```
    

## Usage

### Initialize Token

Run the following command to initialize the token:

```
aptos move run --function aptos_asset::fungible_asset::init_module --args <ADMIN_ADDRESS>
```

### Mint Tokens

```
aptos move run --function aptos_asset::fungible_asset::mint --args <ADMIN_ADDRESS> <TO_ADDRESS> <AMOUNT>
```

### Transfer Tokens

```
aptos move run --function aptos_asset::fungible_asset::transfer --args <ADMIN_ADDRESS> <FROM_ADDRESS> <TO_ADDRESS> <AMOUNT>
```

### Burn Tokens

```
aptos move run --function aptos_asset::fungible_asset::burn --args <ADMIN_ADDRESS> <FROM_ADDRESS> <AMOUNT>
```

### Freeze Account

```
aptos move run --function aptos_asset::fungible_asset::freeze_account --args <ADMIN_ADDRESS> <ACCOUNT_ADDRESS>
```

### Unfreeze Account

```
aptos move run --function aptos_asset::fungible_asset::unfreeze_account --args <ADMIN_ADDRESS> <ACCOUNT_ADDRESS>
```

## License

This project is licensed under the MIT License.
