# aa-aa-exchanger
AA asset to asset exchange

Allows users to exchange an asset for any other asset.

It is not designed to be used directly on wallet (althrough bounce messages help a lot, it is not enough), also it would need integration with DANAA or some kind of asset registry to be more useful.

It is designed to be used through a web, to show data and help filling fields.

It uses also a fool asset representing byte, (deployed on AA `7T3MIJFUUZD23DZJ6BDDGBZPNS6RYFAM`) to allow exchange between assets and bytes. To use it, set `want` param with "bytes" value

Orders are final, or it is filled entirely or it is cancelled.

## Create order
Send asset to offer

Set asset to ask for with `want`

Set price with `price`

![Create order cap](https://i.imgur.com/UmBLjbB.png)

AA will keep your bytes and assets until order be filled or cancelled.


## Cancel order
Set `cancel` = 1

Set offered asset with `asset`

Set ask asset with `want`

Set order price previously set with `price`

![Cancel order cap](https://i.imgur.com/NUpJdTU.png)

AA will send assets previously deposited and your bytes less 1400 fee.



## Check if there are orders to fill
Set `check_fill` = 1

Send asset to offer

Set asset to ask with `want`

Set price to check with `price`

![Check order cap](https://i.imgur.com/APZuPkg.png)

AA will inform user if there are orders to perform the trade instead of creating order.


## Fill order
To fill an order, user must check for state vars to know address to fill.

Set `fill` = 1

Send asset to offer

Set asset to ask for with `want`

Set order price with `price`

Set address to fill with `price`

![Fill order cap](https://i.imgur.com/6HChw1S.png)

AA will perform exchange of both asset and send bytes less 700 fee to each party.

https://testnetexplorer.obyte.org/#StpvADgBjF53Astw6jr3vDXXp0Hca7ZeEZWRGT7ZLpE=
YVTTJBYCQJUILLIHR6XUEQQVJG3EEQLG
