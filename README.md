# API-explorer
FastyChain api explorer

# EXAMPLE
**REQUEST**
/address/{address} (https://fastychain.com/api/address/0x0000000000000000000000000000000000000000)
**RESPONSE**
address
balance *(ETHER format)*
balance_wei *(WEI format)*
updated_at *(YYYY-MM-GG T HOUR:MIN:SECONDS)*
total_supply *(for smart contracts)*
contract *(Is a contract?)*
erc_types *(for smart contracts)*
interfaces *(for smart contracts)*
number_of transactions
attached_contract *(details about compile/verify of the contract, if "valid": false, smart contract not verified.)*

# LIST
**GET REQUESTS**

**ADDRESS**
/address/{address}/transactions
/address/{address}/owned_tokens
/address/{address}/holders
/address/{address}
/address/{address}/internal_transactions
/address/{address}/contract
/address/{address}/tx/{nonce}
/address/{address}/tx/{nonce}/hash

**BLOCKS**
/blocks/{num}/transactions
/blocks/{hash}
/blocks/{num}
/blocks

**GENERAL**
/stats
/richlist
/signersStats
/transaction/{hash}
/signersList
/supply

**POST REQUEST**
/verify
```
{
    "address": "", //contract address
    "contract_name": "", 
    "compiler_version": "0.5.16", //solidity version
    "evm_version": "byzantium",
    "optimization": true, //(bool)
    "source_code": "" //source code, replace enter with \n and " with \"
}
```
