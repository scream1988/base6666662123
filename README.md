# base6666662123
Identifying New Active Wallets Per Day
active = set()

block = w3.eth.get_block("latest", full_transactions=True)
for tx in block.transactions:
    active.add(tx["from"])

print("Active wallets:", len(active))
