---
title: Escribir el método - ActiveX Data Objects (ADO)
TOCTitle: Write Method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98af810c9a24d38a6b2b32db31f9a650c2d6f70a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486086"
---
# <a name="write-method-ado"></a>Write (método, ADO)


**Se aplica a**: Access 2013 | Office 2013


Escribe datos binarios en un objeto [Stream](stream-object-ado.md).

## <a name="syntax"></a>Sintaxis

*Secuencia*. *Búfer* de escritura

## <a name="parameters"></a>Parámetros

  - *Buffer*

  - **Variant** que contiene la matriz de bytes que se va a escribir.

## <a name="remarks"></a>Comentarios

Los bytes especificados se escriben en el objeto **Stream** sin espacios intermedios entre ellos.

El valor de [Position](position-property-ado.md) actual está establecido en el byte situado después de los datos escritos. El método **Write** no trunca el resto de los datos en una secuencia. Si desea truncar estos bytes, llame a [SetEOS](seteos-method-ado.md).

Si escribe más allá de la actual posición de [EOS](eos-property-ado.md), el valor de [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) del objeto **Stream** se incrementará para que pueda contener los bytes nuevos, y ** EOS** se moverá hasta el último byte nuevo en el objeto **Stream**.


> [!NOTE]
> <P>El método <STRONG>Write</STRONG> se utiliza con secuencias binarias (el valor de <A href="type-property-ado-stream.md">Type</A> es <STRONG>adTypeBinary</STRONG>). Utilice <A href="writetext-method-ado.md">WriteText</A> para las secuencias de texto (el valor de <STRONG>Type</STRONG> es <STRONG>adTypeText</STRONG>).</P>


