---
title: Number (propiedad, ADO)
TOCTitle: Number property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5eb46d6fbeb677e6d0fe73223d74ae2ea42d368
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288577"
---
# <a name="number-property-ado"></a>Number (propiedad, ADO)


**Se aplica a:** Access 2013, Office 2013

Indica el número que identifica de forma exclusiva a un objeto [Error](error-object-ado.md).

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **Long** que puede corresponder a una de las constantes [ErrorValueEnum](errorvalueenum.md).

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Number** para determinar el error que se ha producido. El valor de la propiedad es un número exclusivo que corresponde a la condición de error.

La colección [Errors](errors-collection-ado.md) devuelve un HRESULT en formato hexadecimal (por ejemplo, 0x80004005) o en valor de tipo long (por ejemplo, 2147467259). Estos HRESULT pueden ser generados por los componentes subyacentes, como OLE DB o incluso el propio OLE. Para obtener más información acerca de estos números, vea el capítulo 16 de la *Referencia del programador de OLE DB.*

