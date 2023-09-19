# Crypto Wallet

![](22ROOSE-master768.gif)  
<sub>Illustration for Glenn Harvey</sub>

# Criteria A: Planning

## Problem definition

Ms. Sato is a local trader who is interested in the emerging market of cryptocurrencies. She has started to buy and sell electronic currencies, however at the moment she is tracking all his transaction using a ledger in a spreadsheet which is starting to become burdensome and too disorganized. It is also difficult for Ms Sato to find past transactions or important statistics about the currency. Ms Sato is in need of a digital ledger that helps her track the amount of the cryptocurrency, the transactions, along with useful statistics. 

Apart for this requirements, Ms Sato is open to explore a cryptocurrency selected by the developer.
| Name   | Coin            |   | Name | Coin |
|--------|-----------------|---|------|------|
| Keeler | ETH             |   |      |      |
| Rocky  | DOGE            |   |      |      |
| Yuiko  | BNB(Binance)    |   |      |      |
| Jan    | Tether (USDT)   |   |      |      |
| Antoni | XRP(Ripple)     |   |      |      |
| Victor | Cardano (ADA)   |   |      |      |
| Manaha | LTC (LIte Coin) |   |      |      |
| Marina | Solano (SOL)    |   |      |      |
| May    | (DAI)           |   |      |      |
| Ayane  | Zcash (ZEC)     |   |      |      |
| Yosuke  | USD COIN  (USDC)  |   |      |      |
| Naomi  |  TRX Tron       |   |      |      |
| Amine  |  KLIMA          |   |      |      |

| Dylan  | Monero XMR    |   |      |      |
| Yoshi  | Shiba Inu (SHIB)    |   |      |      |


An example of the data stored is 

| Date | Description | Category | Amount  |
|------|-------------|----------|---------|
| Sep 23 2022 | bought a house | Expenses | 10 BTC |
| Sep 24 2022 | food for house celebration | Food | 0.000001 BTC |


## Proposed Solution

Design statement:
I will to design and make a ———— for a client who is ———. The ——– will about ———— and is constructed using the software ———. It will take  ———- to make and will be evaluated according to the criteria ———.

** add a description of your coin and citation **

Justify the tools/structure of your solution

## Success Criteria
1. The electronic ledger is a text-based software (Runs in the Terminal).
2. The electronic ledger display the basic description of the cyrptocurrency selected.
3. The electronic ledger allows to enter, withdraw and record transactions.
4. The graph which shows the rate
5. The graph which shows the benefit (the difference between the rate person bought and now)
6. The chart compared with other electric money

# Criteria B: Design

## System Diagram

## Flow Diagrams
[image]
**Fig. 1** This is the flow diagram for the login system

## Record of Tasks
| Task No | Planned Action        | Planned Outcome                                                                          | Time estimate | Target completion date | Criterion |
|---------|-----------------------|------------------------------------------------------------------------------------------|---------------|------------------------|-----------|
| 1       | Create system diagram | To have a clear idea of the hardware and software requirements for the proposed solution | 10min         | Sep 24                 | B         |
| 2       | Create a login System | To have a flow diagram and the code for the login system                                 | 30 min        | Sep 14                 | B, C      |

# Criteria C: Development

## Login System
My client requires a system to protect the private data. I thought about using a login system to accomplish this requirement using a if condition and the open command to work with a csv file. 

AS you can sere in the flow diagram in **Fig 1**, In th first line I am defining a function called try_login, this function has two inputs of type string, and the output is a boolean representing True if the
user logins correctly or false otherwise. This is saved in the variable success. Then in line two...this is your work.
```.py
def try_login(name:str, password:str)->bool:
    with open('user.csv',mode='r') as f:
        data = f.readlines()

    success = False
    for line in data:
        uname = line.split(',')[0]
        upass = line.split(',')[1].strip() #strip() removes \n
        if uname == name and upass == password:
            success = True
            break
    return success

```
