---
title: ActiveCommand (propiedad, ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 473a0b99310d2eb5e050ed50f1e331cb65174ae8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869564"
---
# <a name="activecommand-property-ado"></a>ActiveCommand (propiedad, ADO)

**Se aplica a**: Access 2013, Office 2013

Indica el objeto [Command](command-object-ado.md) que ha creado el objeto [Recordset](recordset-object-ado.md) asociado.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **Variant** que contiene un objeto **Command**. El valor predeterminado es una referencia de objeto nula.

## <a name="remarks"></a>Comentarios

La propiedad **ActiveCommand** es de sólo lectura.

Si un objeto **Command** no se usó para crear el **objeto Recordset**actual, se devuelve una referencia de objeto **Null** .

Use esta propiedad para buscar el objeto **Command** asociado cuando solo dispone del objeto **Recordset** resultante.

