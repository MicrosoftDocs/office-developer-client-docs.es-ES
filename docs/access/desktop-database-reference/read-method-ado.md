---
title: 'Método Read: ActiveX data objects (ADO)'
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ce545b1a6b036cae9f92d7e1ab7ba7479e4e252
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307675"
---
# <a name="read-method-ado"></a>Método Read (ADO)

**Se aplica a:** Access 2013, Office 2013

Lee un número especificado de bytes de un objeto [Stream](stream-object-ado.md) binario.

## <a name="syntax"></a>Sintaxis

*Variant*  =  *Stream*. Read (*NumBytes* )

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*NumBytes* |Es opcional. Valor de tipo **Long** que especifica el número de bytes que se van a leer en el archivo, o bien, el valor [adReadAll](streamreadenum.md) de **StreamReadEnum**, que es el valor predeterminado.|

## <a name="return-value"></a>Valor devuelto

El método **Read** lee un número especificado de bytes o toda la secuencia de un objeto **Stream** y devuelve los datos resultantes como un valor de tipo **Variant**.

## <a name="remarks"></a>Comentarios

Si el valor de *NumBytes* es mayor que el número de bytes que quedan en el objeto **Stream**, se devolverán sólo los bytes restantes. Los datos leídos no se rellenan para que coincidan con la longitud especificada por *NumBytes*. Si ya no quedan bytes para leer, se devuelve un valor de tipo Variant con el valor null. El método **Read** no se puede utilizar para leer hacia atrás.

> [!NOTE]
> *NumBytes* siempre mide los bytes. En el caso de los objetos **Stream** de texto (el valor de [Type](type-property-ado-stream.md) es **adTypeText**), utilice [ReadText](readtext-method-ado.md).


