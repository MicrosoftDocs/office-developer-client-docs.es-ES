---
title: Number (propiedad, ADO)
TOCTitle: Number Property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4e9b048643b1892197f610ef6d53e6ba46b170d8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483326"
---
# <a name="number-property-ado"></a>Number (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013

Indica el número que identifica de forma exclusiva a un objeto [Error](error-object-ado.md).

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **Long** que puede corresponder a una de las constantes [ErrorValueEnum](errorvalueenum.md).

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Number** para determinar el error que se ha producido. El valor de la propiedad es un número exclusivo que corresponde a la condición de error.

La colección [Errors](errors-collection-ado.md) devuelve un HRESULT en formato hexadecimal (por ejemplo, 0x80004005) o en valor de tipo long (por ejemplo, 2147467259). Estos HRESULT pueden ser generados por los componentes subyacentes, como OLE DB o incluso el propio OLE. Para obtener más información acerca de estos números, consulte el capítulo 16 de la *referencia del programador de OLE DB.*

