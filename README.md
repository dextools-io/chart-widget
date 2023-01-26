# DEXTools chart widget

(This is the public documentation repo of the DEXTools Chart Widget)

The **Chart Widget** allows websites to display an embedded trading chart for any pool supported by [DEXTools.io](www.dextools.io) app. Chart data is updated in real-time, including the current price in USD.


<img src="https://user-images.githubusercontent.com/4454927/214917462-8fe2e9d5-e20a-428a-8771-f557457bb7a9.jpg" width="400">



## Get your pool/token iframe widget code

1) First search your favorite token or pool by address, name... using the [DEXTools search bar](https://www.dextools.io/app/).

<img src="https://user-images.githubusercontent.com/4454927/214916772-39721553-5518-4441-9c5c-49c8283141e6.jpg" width="400">


2) Then click the **share** option of the [DEXTools pair explorer](https://www.dextools.io/app/en/ether/pair-explorer/0xa29fe6ef9592b5d408cca961d0fb9b1faf497d6d), a pop-up will appear with the code to copy.

<img src="https://user-images.githubusercontent.com/4454927/214918425-85d61426-cd1d-4896-9ea0-01691e8a5f92.jpg" width="400">


## Quick Example

A iframe based integration example follows:

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>DEXTools Pair Explorer Widget Template</title>
</head>

<body>

   <iframe id="dextools-widget"
    title="DEXTools Trading Chart"
    width="500"
    height="400" src="https://www.dextools.io/widgets/en/ether/pe-light/0xa29fe6ef9592b5d408cca961d0fb9b1faf497d6d?theme=light&chartType=2&chartResolution=30&drawingToolbars=false"></iframe>

</body>
</html>

```



## Customization options

The widget is configured adjusting following parts and query parameters of this URL:

```
https://www.dextools.io/widgets/en/<chainId>/pe-light/<pairAddress>?theme=<theme>&chartType=<chartType>&chartResolution=<chartResolution>&drawingToolbars=<drawingToolbars>
```

| Parameter       | Values                                                      |
| --------------- | ----------------------------------------------------------- |
| chainId         | blockchain ID (see list below)                              |
| pairAddress     | address of the pool to display                              |
| theme           | dark or light                                               |
| chartType       | 0, 1, 2, 3, 8, 9, 10                                        |
| chartResolution | 1 (minute), 3, 5, 15, 30, 60, 120, 240, 720, 1D, 3D, 1W, 1M |
| drawingToolbars | false or true                                               |

## Supported blockchains

We add support for new blockchains frequently. This is the current list of available blockchains:

| Blockchain   | ID            |
| ------------ | ------------- |
| ETHEREUM     |  ether        |
| BNB          |  bsc          |
| POLYGON      |  polygon      |
| FANTOM       |  fantom       |
| CRONOS       |  cronos       |
| AVALANCHE    |  avalanche    |
| VELAS        |  velas        |
| OASIS        |  oasis        |
| KUCOIN       |  kucoin       |
| METIS        |  metis        |
| OPTIMISM     |  optimism     |
| ARBITRUM     |  arbitrum     |
| CELO         |  celo         |
| TELOS        |  telos        |
| AURORA       |  aurora       |
| MOONBEAM     |  moonbeam     |
| MOONRIVER    |  moonriver    |
| HARMONY      |  harmony      |
| FUSE         |  fuse         |
| HECO         |  heco         |
| OEC          |  oec          |
| ASTAR        |  astar        |
| KLAYTN       |  klaytn       |
| IOTEX        |  iotex        |
| MILKOMEDA    |  milkomeda    |
| DFK          |  dfk          |
| SOLANA       |  solana       |
| EVMOS        |  evmos        |
| DOGECHAIN    |  dogechain    |
| ETC          |  etc          |
| GNOSIS       |  gnosis       |
| BITGERT      |  bitgert      |
| CANTO        |  canto        |
| FLARE        |  flare        |
| ARBITRUMNOVA |  arbitrumnova |
| REDLIGHT     |  redlight     |
| CONFLUX      |  conflux      |
| SMARTBCH     |  smartbch     |
| KARDIA       |  kardia       |
| TOMB         |  tomb         |
| WAN          |  wan          |
| BOBA         |  boba         |
| ELASTOS      |  elastos      |
| NOVA         |  nova         |
| HOO          |  hoo          |
| SHIDEN       |  shiden       |
| FUSION       |  fusion       |
| RSK          |  rsk          |
| CUBE         |  cube         |
| SYSCOIN      |  syscoin      |
| KAVA         |  kava         |
| THUNDERCORE  |  thundercore  |
| ECHELON      |  echelon      |
| METER        |  meter        |
| KEK          |  kek          |
| TOMO         |  tomo         |
| RONIN        |  ronin        |
| SHIB         |  shib         |
| ETHW         |  ethw         |
| ETHF         |  ethf         |
| MUU          |  muu          |
| SX           |  sx           |
| ALVEY        |  alvey        |
| APTOS        |  aptos        |
| MULTIVERSX   |  elrond       |

