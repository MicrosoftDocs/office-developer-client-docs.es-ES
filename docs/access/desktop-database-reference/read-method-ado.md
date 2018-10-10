---
title: Lea el método - ActiveX Data Objects (ADO)
TOCTitle: Read Method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4fcc4c3039e1e55bb6bd33078542faa880d27ded
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484498"
---
# <a name="read-method-ado"></a>Read (método, ADO)


**Se aplica a**: Access 2013 | Office 2013

Lee un número especificado de bytes de un objeto [Stream](stream-object-ado.md) binario.

## <a name="syntax"></a>Sintaxis

*Variant* = *secuencia*. Lectura (*NumBytes* )

## <a name="parameters"></a>Parámetros

  - *NumBytes*

  - Es opcional. Valor de tipo **Long** que especifica el número de bytes que se van a leer en el archivo, o bien, el valor [adReadAll](streamreadenum.md) de **StreamReadEnum**, que es el valor predeterminado.

## <a name="return-value"></a>Valor devuelto

El método **Read** lee un número especificado de bytes o toda la secuencia de un objeto **Stream** y devuelve los datos resultantes como un valor de tipo **Variant**.

## <a name="remarks"></a>Comentarios

Si el valor de *NumBytes* es mayor que el número de bytes que quedan en el objeto **Stream**, se devolverán sólo los bytes restantes. Los datos leídos no se rellenan para que coincidan con la longitud especificada por *NumBytes*. Si ya no quedan bytes para leer, se devuelve un valor de tipo Variant con el valor null. El método **Read** no se puede utilizar para leer hacia atrás.


> [!NOTE]
> <P><EM>NumBytes</EM> siempre mide los bytes. En el caso de los objetos <STRONG>Stream</STRONG> de texto (el valor de <A href="type-property-ado-stream.md">Type</A> es <STRONG>adTypeText</STRONG>), utilice <A href="readtext-method-ado.md">ReadText</A>.</P>


