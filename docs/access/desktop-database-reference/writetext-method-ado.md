---
title: WriteText (método, ADO)
TOCTitle: WriteText Method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 67dcf218814f938c4583ba9587085cff73066dc1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486732"
---
# <a name="writetext-method-ado"></a>WriteText (método, ADO)


**Se aplica a**: Access 2013 | Office 2013

Escribe una cadena de texto especificada en un objeto [Stream](stream-object-ado.md).

## <a name="syntax"></a>Sintaxis

*Secuencia*. WriteText*datos*, *Opciones*

## <a name="parameters"></a>Parámetros

  - *Data*

  - Valor de tipo **String** que contiene el texto en caracteres que se va a escribir.

  - *Options*

  - Es opcional. Valor de [StreamWriteEnum](streamwriteenum.md) que especifica si debe escribirse un carácter separador de línea al final de la cadena especificada.

## <a name="remarks"></a>Comentarios

Las cadenas especificadas se escriben en el objeto **Stream** sin espacios ni caracteres intermedios entre ellas.

El valor de [Position](position-property-ado.md) actual está establecido en el carácter situado después de los datos escritos. El método **WriteText** no trunca el resto de los datos en una secuencia. Si desea truncar estos caracteres, llame a [SetEOS](seteos-method-ado.md).

Si escribe más allá de la actual posición de [EOS](eos-property-ado.md), el valor de [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) del objeto **Stream** se incrementará para que pueda contener los caracteres nuevos, y ** EOS** se moverá hasta el último byte nuevo en el objeto **Stream**.


> [!NOTE]
> <P>El método <STRONG>WriteText</STRONG> se utiliza para las secuencias de texto (el valor de <A href="type-property-ado-stream.md">Type</A> es <STRONG>adTypeText</STRONG>). En el caso de las secuencias binarias (el valor de <STRONG>Type</STRONG> es <STRONG>adTypeBinary</STRONG>), utilice <A href="write-method-ado.md">Write</A>.</P>


