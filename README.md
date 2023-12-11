<p align="center">
    <h1 align="center">PROJECT KEMET - CASH AS ITEM</h1>
    <h2 align="center">The easiest cash & blackmoney item script for qbcore servers</h2>
</p>


# Original Script

- [mh-cashasitem](https://github.com/MaDHouSe79/mh-cashasitem)


# pk-cashasitem

- Use cash or blackmonmey as item for qb-core
- Blackmoney item as option you can use instead of MarkedBills
- Works with any inventory system
- Works with any banking system


# Dependencies

- [qb-core](https://github.com/qbcore-framework/qb-core)


# Install

- Put `pk-cashasitem` into your resources folder or any folder you want,
- In your server.cfg add > `ensure pk-cashasitem`,
- Enjoy


# Command

- /blackmoney to see the amount
- /cash to see the amount


# If you are using blackmoney as an item

- Add blackmoney to qbcore > config.lua
```lua
QBConfig.Money.MoneyTypes = { cash = 500, bank = 5000, crypto = 0, blackmoney = 0 } -- type = startamount - Add or remove money types for your server (for ex. blackmoney = 0), remember once added it will not be removed from the database!
QBConfig.Money.DontAllowMinus = { 'cash', 'crypto', 'blackmoney' } -- Money that is not allowed going in minus
```


# Add in `[qb]/qb-core/shared/items.lua` 

```lua
['cash'] = {
    ['name'] = 'cash', 
    ['label'] = 'Cash', 
    ['weight'] = 0, 
    ['type'] = 'item', 
    ['image'] = 'cash.png', 
    ['unique'] = false,
    ['useable'] = false,
    ['shouldClose'] = true,
    ['combinable'] = nil,
    ['description'] = 'Cash'
},
['blackmoney'] = {
    ['name'] = 'blackmoney',
    ['label'] = 'Black Money',
    ['weight'] = 0,
    ['type'] = 'item',
    ['image'] = 'blackmoney.png',
    ['unique'] = false,
    ['useable'] = false,
    ['shouldClose'] = true,
    ['combinable'] = nil,
    ['description'] = 'Black Money?'
},
```


# LICENSE

[MIT LICENSE](./LICENSE)