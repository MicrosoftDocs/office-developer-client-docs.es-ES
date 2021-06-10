---
title: Método ReadText (ADO)
TOCTitle: ReadText method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 883f74c06da83a46f9ffd1c30861d796c04b5c74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300801"
---
# <a name="readtext-method-ado"></a>Método ReadText (ADO)

**Se aplica a:** Access 2013, Office 2013

Lee un número especificado de caracteres de un objeto [Stream](stream-object-ado.md) de texto.

## <a name="syntax"></a>Sintaxis

*String*  =  *Stream*. ReadText (*NumChars*)

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*NumChars* |Es opcional. Valor de tipo **Long** que especifica el número de caracteres que se van a leer en el archivo o un valor de [StreamReadEnum](streamreadenum.md). El valor predeterminado es **adReadAll**.|

## <a name="return-value"></a>Valor devuelto

El método **ReadText** lee un número especificado de caracteres, una línea completa o toda la secuencia de un objeto **Stream** y devuelve la cadena resultante.

## <a name="remarks"></a>Comentarios

Si el valor de *NumChar* es mayor que el número de caracteres que quedan en la secuencia, se devuelven sólo los caracteres restantes. La cadena leída no se rellena para que coincida con la longitud especificada por *NumChar*. Si no quedan caracteres para leer, se devuelve un valor de tipo Variant con el valor null. **ReadText** no se puede utilizar para leer hacia atrás.

> [!NOTE]
> El método **ReadText** se utiliza para las secuencias de texto (el valor de [Type](type-property-ado-stream.md) es **adTypeText**). En el caso de las secuencias binarias (el valor de **Type** es **adTypeBinary**), utilice [Read](read-method-ado.md).

