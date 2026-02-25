# DEXTools chart widget

(This is the public documentation repo of the DEXTools Chart Widget)

The **Chart Widget** allows websites to display an embedded trading chart for any pool supported by [DEXTools.io](https://www.dextools.io) app. Chart data is updated in real-time, including the current price in USD.

<img width="882" height="538" alt="widget screenshot" src="https://github.com/user-attachments/assets/54b9c56f-d453-443d-a92d-5cd754de917e" />

Chart display is provided by [TradingView](https://www.tradingview.com/)


## Get your pool/token iframe widget code

1) First search your favorite token or pool by address, name... using the [DEXTools search bar](https://www.dextools.io/app/).

<img width="1127" height="315" alt="search screenshot" src="https://github.com/user-attachments/assets/108969c7-596a-4482-8976-f11fef4a1d5b" />


2) Then click the **embed** option of the [DEXTools pair explorer](https://www.dextools.io/app/en/ether/pair-explorer/0xa29fe6ef9592b5d408cca961d0fb9b1faf497d6d), a pop-up will appear to configure the chart and copy the embed code.

<img width="376" height="375" alt="embed screenshot" src="https://github.com/user-attachments/assets/c99decc2-00ac-479b-8898-ca074eb55110" />


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

The widget is configured by using the embed wizard, but also manually adjusting the following parts and query parameters of this URL:

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

| Blockchain | ID |
| :--- | :--- |
| SOLANA | solana |
| ETHEREUM | ether |
| BNB | bnb |
| BASE | base |
| POLYGON | polygon |
| PULSE | pulse |
| TON | ton |
| ARBITRUM | arbitrum |
| AVALANCHE | avalanche |
| MONAD | monad |
| RONIN | ronin |
| SUI | sui |
| SONIC | sonic |
| TRON | tron |
| CRONOS | cronos |
| XRPL | xrpl |
| WORLD CHAIN | worldchain |
| OSMOSIS | osmosis |
| ABSTRACT | abstract |
| VSC | vsc |
| SONEIUM | soneium |
| LINEA | linea |
| OPTIMISM | optimism |
| ICP | icp |
| HYPER EVM | hyperevm |
| BERA CHAIN | berachain |
| X LAYER | xlayer |
| CHILIZ | chiliz |
| SHIBARIUM | shib |
| HEDERA | hedera |
| APTOS | aptos |
| MANTLE | mantle |
| UNI CHAIN | unichain |
| SHIDO | shido |
| FLARE | flare |
| METIS | metis |
| DOGE CHAIN | dogechain |
| ZKSYNC | zksync |
| STORY | story |
| KAIA | kaia |
| NEAR | near |
| INK | ink |
| CELO | celo |
| PLASMA | plasma |
| SEI | sei |
| XDC | xdc |
| GNOSIS | gnosis |
| APE CHAIN | apechain |
| IOTA-EVM | iotaevm |
| BLAST | blast |
| INJECTIVE | injective |
| QUBIC | qubic |
| ETHERLINK | etherlink |
| PAW CHAIN | pawchain |
| FUSE | fuse |
| U2U | utwou |
| ODYSSEY | odyssey |
| SCROLL | scroll |
| CRONOS-ZKEVM | cronoszkevm |
| SUPERSEED | superseed |
| OKTC (FORMER OEC) | oktc |
| ARBITRUM NOVA | arbitrumnova |
| BITLAYER | bitlayer |
| ELYSIUM | elysium |
| GRAVITY ALPHA | gravityalpha |
| MODE | mode |
| MANTA | manta |
| KAVA | kava |
| KUJIRA | kujira |
| POLYGON-ZKEVM | polygonzkevm |
| UNIT ZERO | units |
| NIBIRU | nibiruevm |
