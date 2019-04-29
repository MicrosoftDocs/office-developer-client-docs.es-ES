---
title: Constantes de moneda
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82253123
localization_priority: Normal
ms.assetid: d94c740f-29e1-1e7f-39f6-8aa215f3111d
description: Para dar formato de moneda a un número, puede utilizar la función CY y pasar una constante opcional que determine de qué moneda se trata. Las constantes de moneda pueden especificarse como el número de Id. que corresponde a un país o región o como una cadena entre comillas que corresponda a la abreviatura de tres caracteres de la norma ISO 4217.
ms.openlocfilehash: 4492f4901779d94a32b881c973eab9e32a9c0514
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421798"
---
# <a name="about-currency-constants"></a>Constantes de moneda

Para dar formato de moneda a un número, puede utilizar la función CY y pasar una constante opcional que determine de qué moneda se trata. Las constantes de moneda pueden especificarse como el número de Id. que corresponde a un país o región o como una cadena entre comillas que corresponda a la abreviatura de tres caracteres de la norma ISO 4217.
  
Si muestra símbolos de monedas no locales y el sistema no conoce el que corresponde a una de ellas, aparecerá en su lugar el símbolo de dólar ($).
  
## <a name="ids-and-abbreviations"></a>Identificadores y abreviaturas

|**ID**|**Abbreviation**|**Moneda**|
|:-----|:-----|:-----|
| comprendi  <br/> | PET  <br/> | Utiliza la configuración del sistema  <br/> |
| 1  <br/> | XXX  <br/> | Da formato como número  <br/> |
| 2 -9  <br/> | Reserved  <br/> |
| 10   <br/> | EUR  <br/> | Euro  <br/> |
| 11   <br/> | EUR  <br/> | Dólar de EE.UU.  <br/> |
| 12  <br/> | ATS  <br/> | Chelín austriaco  <br/> |
| 13   <br/> | AUD  <br/> | Dólar australiano  <br/> |
| 14   <br/> | BEF  <br/> | Franco belga  <br/> |
| 15   <br/> | CAD  <br/> | Dólar canadiense  <br/> |
| 16   <br/> | CHF  <br/> | Franco suizo  <br/> |
| 17   <br/> | CNY  <br/> | Yuan renminbi chino  <br/> |
| 18   <br/> | DEM  <br/> | Marco alemán  <br/> |
| 18  <br/> | DKK  <br/> | Corona danesa  <br/> |
| 20  <br/> | ESP  <br/> | Peseta española  <br/> |
| 21  <br/> | FIM  <br/> | Marco finlandés  <br/> |
| 22  <br/> | FRF  <br/> | Franco francés  <br/> |
| veintitrés  <br/> | GBP  <br/> | Libra esterlina británica  <br/> |
| apartado  <br/> | GRD  <br/> | Dracma griega  <br/> |
| IVA  <br/> | HKD  <br/> | Dólar de la Región Administrativa Especial de Hong Kong  <br/> |
| apartado  <br/> | HUF  <br/> | Florín húngaro  <br/> |
| ,27  <br/> | Integrated  <br/> | Rupia indonesia  <br/> |
| 28  <br/> | IEP  <br/> | Libra irlandesa  <br/> |
| 32  <br/> | Il  <br/> | Shekel israelí  <br/> |
| semestre  <br/> | ITL  <br/> | Lira italiana  <br/> |
| 31  <br/> | JPY  <br/> | Yen japonés  <br/> |
| 32  <br/> | KRW  <br/> | Won coreano  <br/> |
| 33  <br/> | LUF  <br/> | Franco luxemburgués  <br/> |
| 34  <br/> | PESOS  <br/> | Peso mejicano  <br/> |
| 35  <br/> | MYR  <br/> | Ringgit malayo  <br/> |
| 36  <br/> | NLG  <br/> | Florín neerlandés  <br/> |
| 37  <br/> | NOK  <br/> | Corona noruega  <br/> |
| 38  <br/> | NZD  <br/> | Dólar neozelandés  <br/> |
| 39  <br/> | PHP  <br/> | Peso filipino  <br/> |
| 40  <br/> | PLZ (Histórico. Utilice PLN.)  <br/> | Zloty polaco  <br/> |
| 41  <br/> | PTE  <br/> | Escudo portugués  <br/> |
| 42  <br/> | ROL  <br/> | Leu rumano  <br/> |
| 43  <br/> | RUR (Histórico. Utilice RUB.)  <br/> | Rublo ruso  <br/> |
| 44  <br/> | SEK  <br/> | Corona sueca  <br/> |
| 45  <br/> | SGD  <br/> | Dólar de Singapur  <br/> |
| 46  <br/> | THB  <br/> | Baht tailandés  <br/> |
| 47  <br/> | TWD  <br/> | Nuevo dólar taiwanés  <br/> |
| 48  <br/> | XEU (Histórico. Utilice EUR.)  <br/> | ECU (anterior a 1998)  <br/> |
| 49  <br/> | YUN (Histórico. Utilice YUM.)  <br/> | Dinar yugoslavo  <br/> |
| 50  <br/> | ZAR  <br/> | Rand sudafricano  <br/> |
| 51 -55  <br/> | Reserved  <br/> |
| 56  <br/> | LLEVARÁ  <br/> | Peso argentino  <br/> |
| 57  <br/> | BMD  <br/> | Dólar de las Bermudas  <br/> |
| 58  <br/> | CARGO  <br/> | Bolívar boliviano  <br/> |
| 59  <br/> | BRR (Histórico. Utilice BRL.)  <br/> | Cruceiro brasileño  <br/> |
| 60  <br/> | BSD  <br/> | Dólar de las Bahamas  <br/> |
| 61  <br/> | CLP  <br/> | Peso chileno  <br/> |
| 62  <br/> | COP  <br/> | Peso colombiano  <br/> |
| 63  <br/> | CRC  <br/> | Colón costarricense  <br/> |
| 64  <br/> | CZK  <br/> | Corona checa  <br/> |
| 65  <br/> | DOP  <br/> | Peso dominicano  <br/> |
| 66  <br/> | ECS  <br/> | Sucre ecuatoriano  <br/> |
| 67  <br/> | EGP  <br/> | Libra egipcia  <br/> |
| 68  <br/> | HNL  <br/> | Lempira hondureña  <br/> |
| 69  <br/> | INR  <br/> | Rupia india  <br/> |
| 70  <br/> | JMD  <br/> | Dólar jamaicano  <br/> |
| 71  <br/> | JOD  <br/> | Dinar jordano  <br/> |
| 72  <br/> | KWD  <br/> | Dinar kuwaití  <br/> |
| 73  <br/> | POP  <br/> | Pataca de Macao  <br/> |
| 74  <br/> | NIO  <br/> | Córdoba oro nicaragüense  <br/> |
| 75  <br/> | LPD  <br/> | Balboa panameño  <br/> |
| 76  <br/> | PUNTA  <br/> | Nuevo sol peruano  <br/> |
| 77  <br/> | PKR  <br/> | Rupia pakistaní  <br/> |
| 78  <br/> | PYG  <br/> | Guaraní paraguayo  <br/> |
| 79  <br/> | ADMINISTRATIVAS  <br/> | Rial saudí  <br/> |
| 80  <br/> | TRABAJA  <br/> | Tolar esloveno  <br/> |
| 81  <br/> | SKK  <br/> | Corona eslovaca  <br/> |
| 82  <br/> | SVC  <br/> | Colón salvadoreño  <br/> |
| 83  <br/> | Utilice  <br/> | Nueva lira turca  <br/> |
| 84  <br/> | TT  <br/> | Dólar de Trinidad y Tobago  <br/> |
| 85  <br/> | UYU  <br/> | Peso uruguayo  <br/> |
| 86  <br/> | VEB  <br/> | Bolívar Fuerte  <br/> |
| 87  <br/> | VND  <br/> | Dong vietnamita  <br/> |
| 88  <br/> | BRL  <br/> | Cruceiro brasileño  <br/> |
| 89  <br/> | PLN  <br/> | Zloty polaco  <br/> |
| 90  <br/> | RUB  <br/> | Rublo ruso  <br/> |
| 91  <br/> | YUM  <br/> | Dinar yugoslavo  <br/> |
| 92  <br/> | BYB (Histórico. Utilice BYR.)  <br/> | Rublo bielorruso  <br/> |
| 93  <br/> | UAH  <br/> | Hryvnia ucraniano  <br/> |
| 94  <br/> | AFA  <br/> | Afgani (agregado en Visio 2002)  <br/> |
| 95  <br/> | TODOS  <br/> | Lek (agregado en Visio 2002)  <br/> |
| 96  <br/> | DZD  <br/> | Dinar argelino (agregado en Visio 2002)  <br/> |
| 97  <br/> | ADP  <br/> | Peseta andorrana (agregado en Visio 2002)  <br/> |
| 98  <br/> | AOA  <br/> | Kwanza (agregado en Visio 2002)  <br/> |
| 99  <br/> | XCD  <br/> | Dólar del Caribe oriental (agregado en Visio 2002)  <br/> |
| 100  <br/> | PROCESADOR  <br/> | Dram armenio (agregado en Visio 2002)  <br/> |
| 101  <br/> | AWG  <br/> | Florín arubeño (agregado en Visio 2002)  <br/> |
| 102  <br/> | AZM  <br/> | Manat azerí (agregado en Visio 2002)  <br/> |
| 103  <br/> | BHD  <br/> | Dinar bahriní (agregado en Visio 2002)  <br/> |
| 104  <br/> | BDT  <br/> | Taka (agregado en Visio 2002)  <br/> |
| 105  <br/> | BBD  <br/> | Dólar barbadense (agregado en Visio 2002)  <br/> |
| 106  <br/> | BYR  <br/> | Rublo bielorruso (agregado en Visio 2002)  <br/> |
| 107  <br/> | BZD  <br/> | Dólar beliceño (agregado en Visio 2002)  <br/> |
| 108  <br/> | XOF  <br/> | Franco CFA del BCEAO (agregado en Visio 2002)  <br/> |
| 109  <br/> | BTN  <br/> | Ngultrum (agregado en Visio 2002)  <br/> |
| 110  <br/> | PAM  <br/> | Marcos convertibles (agregado en Visio 2002)  <br/> |
| 111  <br/> | BWP  <br/> | Pula (agregado en Visio 2002)  <br/> |
| 112  <br/> | BND  <br/> | Dólar bruneano (agregado en Visio 2002)  <br/> |
| 113  <br/> | BGL (Histórico. Utilice BGN.)  <br/> | Lev  <br/> |
| 114  <br/> | BGN  <br/> | Lev búlgaro (agregado en Visio 2002)  <br/> |
| 115  <br/> | BIF  <br/> | Franco burundés (agregado en Visio 2002)  <br/> |
| 116  <br/> | KHR  <br/> | Riel (agregado en Visio 2002)  <br/> |
| 117  <br/> | XAF  <br/> | Franco CFA del BEAC (agregado en Visio 2002)  <br/> |
| 118  <br/> | CVE  <br/> | Escudo caboverdiano (agregado en Visio 2002)  <br/> |
| 119  <br/> | KYD  <br/> | Dólar de las Islas Caimán (agregado en Visio 2002)  <br/> |
| 120  <br/> | KMF  <br/> | Franco comorano (agregado en Visio 2002)  <br/> |
| 121  <br/> | CDF  <br/> | Franco congoleño (agregado en Visio 2002)  <br/> |
| 122  <br/> | HRK  <br/> | Kuna croata (agregado en Visio 2002)  <br/> |
| 123  <br/> | BAJA  <br/> | Peso cubano (agregado en Visio 2002)  <br/> |
| 124  <br/> | CYP  <br/> | Libra chipriota (agregado en Visio 2002)  <br/> |
| 125  <br/> | DJF  <br/> | Franco yibutiense (agregado en Visio 2002)  <br/> |
| 126  <br/> | TPE  <br/> | Escudo de Timor (agregado en Visio 2002)  <br/> |
| 127  <br/> | ERN  <br/> | Nafka eritreo (agregado en Visio 2002)  <br/> |
| 128  <br/> | EEK  <br/> | Corona estonia (agregado en Visio 2002)  <br/> |
| 129  <br/> | ETB  <br/> | Birr etíope (agregado en Visio 2002)  <br/> |
| 130  <br/> | FKP  <br/> | Libra de las Islas Malvinas (agregado en Visio 2002)  <br/> |
| 131  <br/> | FJD  <br/> | Dólar fiyiano (agregado en Visio 2002)  <br/> |
| 132  <br/> | XPF  <br/> | Franco CFP (agregado en Visio 2002)  <br/> |
| 133  <br/> | GMD  <br/> | Dalasi (agregado en Visio 2002)  <br/> |
| 134  <br/> | DESLIZA  <br/> | Lari (agregado en Visio 2002)  <br/> |
| 135  <br/> | GHC  <br/> | Cedi (agregado en Visio 2002)  <br/> |
| 136  <br/> | GIP  <br/> | Libra gibraltareña (agregado en Visio 2002)  <br/> |
| 137  <br/> | GTQ  <br/> | Quetzal (agregado en Visio 2002)  <br/> |
| 138  <br/> | GNF  <br/> | Franco guineano (agregado en Visio 2002)  <br/> |
| 139  <br/> | GWP  <br/> | Peso de Guinea-Bissau (agregado en Visio 2002)  <br/> |
| 140  <br/> | GYD  <br/> | Dólar guyanés (agregado en Visio 2002)  <br/> |
| 141  <br/> | HTG  <br/> | Gourde haitiano (agregado en Visio 2002)  <br/> |
| 142  <br/> | ISK  <br/> | Corona islandesa (agregado en Visio 2002)  <br/> |
| 143  <br/> | IRR  <br/> | Rial iraní (agregado en Visio 2002)  <br/> |
| 144  <br/> | IQD  <br/> | Dinar iraquí (agregado en Visio 2002)  <br/> |
| 145  <br/> | KZT  <br/> | Tenge (agregado en Visio 2002)  <br/> |
| 146  <br/> | KES  <br/> | Chelín keniano (agregado en Visio 2002)  <br/> |
| 147  <br/> | KPW  <br/> | Won norcoreano (agregado en Visio 2002)  <br/> |
| 148  <br/> | KGS  <br/> | Som (agregado en Visio 2002)  <br/> |
| 149  <br/> | LAK  <br/> | Kip (agregado en Visio 2002)  <br/> |
| 150  <br/> | COSTO (histórico. Utilice EUR.)  <br/> | Lats de Letonia (agregado en Visio 2002)  <br/> |
| 151  <br/> | LBP  <br/> | Libra libanesa (agregado en Visio 2002)  <br/> |
| 152  <br/> | LSL  <br/> | Loti (agregado en Visio 2002)  <br/> |
| 153  <br/> | LRD  <br/> | Dólar liberiano (agregado en Visio 2002)  <br/> |
| 154  <br/> | LYD  <br/> | Dinar libio (agregado en Visio 2002)  <br/> |
| 155  <br/> | LTL  <br/> | Litus lituano (agregado en Visio 2002)  <br/> |
| 156  <br/> | MKD  <br/> | Denar (agregado en Visio 2002)  <br/> |
| 157  <br/> | MGF (Histórico. Utilice MGA.)  <br/> | Franco malgache (agregado en Visio 2002)  <br/> |
| 158  <br/> | MWK  <br/> | Kwacha de Malaui (agregado en Visio 2002)  <br/> |
| 159  <br/> | MVR  <br/> | Rufiyaa (agregado en Visio 2002)  <br/> |
| 160  <br/> | MTL  <br/> | Lira maltesa (agregado en Visio 2002)  <br/> |
| 161  <br/> | MRO  <br/> | Ouguiya (agregado en Visio 2002)  <br/> |
| 162  <br/> | MUR  <br/> | Rupia mauriciana (agregado en Visio 2002)  <br/> |
| 163  <br/> | SÍNCRONA  <br/> | Leu moldavo (agregado en Visio 2002)  <br/> |
| 164  <br/> | MNT  <br/> | Tugrik mongol (agregado en Visio 2002)  <br/> |
| 165  <br/> | LAS  <br/> | Dirham marroquí (agregado en Visio 2002)  <br/> |
| 166  <br/> | MZM  <br/> | Metical (agregado en Visio 2002)  <br/> |
| 167  <br/> | MMK  <br/> | Kyat (agregado en Visio 2002)  <br/> |
| 168  <br/> | NAD  <br/> | Dólar namibio (agregado en Visio 2002)  <br/> |
| 169  <br/> | NPR  <br/> | Rupia nepalí (agregado en Visio 2002)  <br/> |
| 170  <br/> | ANG  <br/> | Florín de las antillas holandesas (agregado en Visio 2002)  <br/> |
| 171  <br/> | NGN  <br/> | Naira (agregado en Visio 2002)  <br/> |
| 172  <br/> | OMR  <br/> | Rial omaní (agregado en Visio 2002)  <br/> |
| 173  <br/> | PGK  <br/> | Kina (agregado en Visio 2002)  <br/> |
| 174  <br/> | QAR  <br/> | Rial de Qatar (agregado en Visio 2002)  <br/> |
| 175  <br/> | RWF  <br/> | Franco ruandés (agregado en Visio 2002)  <br/> |
| 176  <br/> | NO  <br/> | Libra de Santa Elena (agregado en Visio 2002)  <br/> |
| 177  <br/> | WST  <br/> | Tala (agregado en Visio 2002)  <br/> |
| 178  <br/> | ESTÁNDAR  <br/> | Dobra (agregado en Visio 2002)  <br/> |
| 179  <br/> | SCR  <br/> | Rupia de las Seychelles (agregado en Visio 2002)  <br/> |
| 180  <br/> | SLL  <br/> | Leone sierraleonés (agregado en Visio 2002)  <br/> |
| 181  <br/> | LABOR  <br/> | Dólar salomonense (agregado en Visio 2002)  <br/> |
| 182  <br/> | SOS  <br/> | Chelín somalí (agregado en Visio 2002)  <br/> |
| 183  <br/> | LKR  <br/> | Rupia de Sri Lanka (agregado en Visio 2002)  <br/> |
| 184  <br/> | SDD  <br/> | Dinar sudanés (agregado en Visio 2002)  <br/> |
| 185  <br/> | SRG  <br/> | Florín surinamés (agregado en Visio 2002)  <br/> |
| 186  <br/> | SZL  <br/> | Lilangeni (agregado en Visio 2002)  <br/> |
| 187  <br/> | SYP  <br/> | Libra siria (agregado en Visio 2002)  <br/> |
| 188  <br/> | TJR (Histórico. Utilice TJS.)  <br/> | Rublo tayiko  <br/> |
| 189  <br/> | TJS  <br/> | Somoni tayiko (agregado en Visio 2002)  <br/> |
| 190  <br/> | TZS  <br/> | Chelín tanzano (agregado en Visio 2002)  <br/> |
| 191  <br/> | LADO  <br/> | Pa'anga (agregado en Visio 2002)  <br/> |
| 192  <br/> | TND  <br/> | Dinar tunecino (agregado en Visio 2002)  <br/> |
| 193  <br/> | TMM  <br/> | Manat (agregado en Visio 2002)  <br/> |
| 194  <br/> | UGX  <br/> | Chelín ugandés (agregado en Visio 2002)  <br/> |
| 195  <br/> | AED  <br/> | Dirham de los Emiratos Árabes Unidos (agregado en Visio 2002)  <br/> |
| 196  <br/> | UZS  <br/> | Sum uzbeco (agregado en Visio 2002)  <br/> |
| 197  <br/> | VUV  <br/> | Vatu (agregado en Visio 2002)  <br/> |
| 198  <br/> | YER  <br/> | Rial yemení (agregado en Visio 2002)  <br/> |
| 199  <br/> | ZMK  <br/> | Kwacha zambiano (agregado en Visio 2002)  <br/> |
| 200  <br/> | ZWD  <br/> | Dólar zimbabuense (agregado en Visio 2002)  <br/> |
|201  <br/> |VEF  <br/> |Bolívar fuerte venezolano (agregado en Visio 2010)  <br/> |
|202  <br/> |MGA  <br/> |Ariary malgache (agregado en Visio 2010)  <br/> |
|203  <br/> |RSD  <br/> |Dinar serbio (agregado en Visio 2010)  <br/> |
|204  <br/> |CSD (Historic. Use RSD.)  <br/> |Dinar serbio (agregado en Visio 2010)  <br/> |
   

