# DEXTools chart widget

(This is the public documentation repo of the DEXTools Chart Widget)

The **Chart Widget** allows websites to display an embedded trading chart for any pool supported by [DEXTools.io](https://www.dextools.io) app. Chart data is updated in real-time, including the current price in USD.


<img src="https://user-images.githubusercontent.com/5698318/290871207-2c2d4ccf-b4fb-449e-a0a1-1653dee423c8.png" width="400" alt="widget screenshot">


Chart display is provided by [TradingView](https://www.tradingview.com/)


## Get your pool/token iframe widget code

1) First search your favorite token or pool by address, name... using the [DEXTools search bar](https://www.dextools.io/app/).

<img src="https://user-images.githubusercontent.com/4454927/214916772-39721553-5518-4441-9c5c-49c8283141e6.jpg" width="400" alt="search screenshot">


2) Then click the **share** option of the [DEXTools pair explorer](https://www.dextools.io/app/en/ether/pair-explorer/0xa29fe6ef9592b5d408cca961d0fb9b1faf497d6d), a pop-up will appear with the code to copy.

<img src="https://user-images.githubusercontent.com/4454927/214918425-85d61426-cd1d-4896-9ea0-01691e8a5f92.jpg" width="400" alt="share panel screenshot">


## Quick Example

An iframe based integration example follows:

```html
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
    height="400" src="https://www.dextools.io/widget-chart/en/ether/pe-light/0xa29fe6ef9592b5d408cca961d0fb9b1faf497d6d?theme=light&chartType=2&chartResolution=30&drawingToolbars=false"></iframe>

</body>
</html>

```

## Common issues and testing

You can test if the IFrame integration works properly with the https://iframetester.com/ tool.

In case of errors showing a Chart in your website, please check your CSP policy for IFrame content https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

Please be aware that USE OF CHART WIDGET IFRAME FROM **localhost** WON'T WORK, please use a real domain instead.

## Customization options

The widget is configured adjusting following parts and query parameters of this URL:

```
https://www.dextools.io/widget-chart/en/<chainId>/pe-light/<pairAddress>?theme=<theme>&chartType=<chartType>&chartResolution=<chartResolution>&drawingToolbars=<drawingToolbars>&tvPlatformColor=<color>&tvPaneColor=<color>&headerColor=<color>&chartInUsd=<chartInUsd>
```

| Parameter       | Values                                                                                                                                                |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| chainId         | blockchain ID (see [list below](#supported-blockchains))                                                                                              |
| pairAddress     | address of the pool to display                                                                                                                        |
| theme           | `dark` or `light`                                                                                                                                     |
| chartType       | 0 = Bar<br/>1 = Candle<br/>2 = Line<br/>3 = Area<br/>8 = Heikin Ashi<br/>9 = hollow candle<br/>10 = Baseline                                          |
| chartResolution | 1 (minute), 3, 5, 15, 30, 60, 120, 240, 720, 1D, 3D, 1W, 1M                                                                                           |
| drawingToolbars | `false` or `true`                                                                                                                                     |
| headerColor     | custom color for the widget header.<br/>**IMPORTANT: should be in hexadecimal format without the `#`**                                                |
| tvPlatformColor | custom color for the chart background.<br/>**IMPORTANT: should be in hexadecimal format without the `#`**                                             |
| tvPaneColor     | custom color for the chart controls background.<br/>**IMPORTANT: should be in hexadecimal format without the `#`**                                    |
| chartInUsd      | `false` to show the "Token/\<chain reference token\>" chart, otherwise (also if this param is not passed) the chart is the "Token/USD" one by default |


## Supported blockchains

We add support for new blockchains frequently. This is the current list of available blockchains:

| Blockchain                 | ID           |
|----------------------------|--------------|
| ETHEREUM                   | ether        |
| BNB                        | bnb          |
| POLYGON                    | polygon      |
| FANTOM                     | fantom       |
| CRONOS                     | cronos       |
| AVALANCHE                  | avalanche    |
| VELAS                      | velas        |
| OASIS                      | oasis        |
| KCC                        | kucoin       |
| METIS                      | metis        |
| OPTIMISM                   | optimism     |
| ARBITRUM                   | arbitrum     |
| CELO                       | celo         |
| TELOS                      | telos        |
| AURORA                     | aurora       |
| MOONBEAM                   | moonbeam     |
| MOONRIVER                  | moonriver    |
| HARMONY                    | harmony      |
| FUSE                       | fuse         |
| HECO                       | heco         |
| OKTC (FORMER OEC)          | oktc         |
| ASTAR                      | astar        |
| KLAYTN                     | klaytn       |
| IOTEX                      | iotex        |
| MILKOMEDA                  | milkomeda    |
| AVAX DFK                   | dfk          |
| SOLANA                     | solana       |
| EVMOS                      | evmos        |
| DOGE CHAIN                 | dogechain    |
| ETHEREUM CLASSIC           | etc          |
| GNOSIS                     | gnosis       |
| BITGERT                    | bitgert      |
| CANTO                      | canto        |
| FLARE                      | flare        |
| ARBITRUM NOVA              | arbitrumnova |
| REDLIGHT                   | redlight     |
| CONFLUX                    | conflux      |
| SMARTBCH                   | smartbch     |
| KARDIA                     | kardia       |
| TOMB                       | tomb         |
| WAN                        | wan          |
| BOBA                       | boba         |
| ELASTOS                    | elastos      |
| NOVA                       | nova         |
| HOO                        | hoo          |
| SHIDEN                     | shiden       |
| FUSION                     | fusion       |
| RSK                        | rsk          |
| CUBE                       | cube         |
| SYSCOIN                    | syscoin      |
| KAVA                       | kava         |
| THUNDERCORE                | thundercore  |
| ECHELON                    | echelon      |
| METER                      | meter        |
| KEK                        | kek          |
| TOMO                       | tomo         |
| RONIN                      | ronin        |
| SHIB                       | shib         |
| ETHEREUM POW               | ethw         |
| DIS (FORMER ETHEREUM FAIR) | dis          |
| MUU                        | muu          |
| SX                         | sx           |
| ALVEY                      | alvey        |
| APTOS                      | aptos        |
| MULTIVERSX (FORMER ELROND) | multiversx   |
| PROOF OF MEMES             | pom          |
| EXOSAMA                    | exosama      |
| ENERGI                     | energi       |
| GOERLI                     | ethergoerli  |
| CORE DAO                   | coredao      |
| FILECOIN                   | filecoin     |
| ZKSYNC                     | zksync       |
| POLYGON-ZKEVM              | polygonzkevm |
| PULSE                      | pulse        |
| LINEA                      | linea        |
| BASE                       | base         |
| MANTLE                     | mantle       |
| BITROCK                    | bitrock      |
| OPBNB                      | opbnb        |
| SHIBARIUM                  | shib         |
| STARKNET                   | starknet     |
| SCROLL                     | scroll       |
| MANTA                      | manta        |
| KUJIRA                     | kujira       |
| BLAST                      | blast        |
| BITTORRENT                 | bittorrent   |
| OSMOSIS                    | osmosis      |
| X LAYER                    | xlayer       |
| SHIMMEREVM                 | shimmer      |
| MODE                       | mode         |
| TON                        | ton          |
| HEDERA                     | hedera       |
| NEAR                       | near         |
