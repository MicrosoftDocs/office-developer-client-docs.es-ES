---
title: ActiveCommand (propiedad, ADO)
TOCTitle: ActiveCommand Property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f01ae4c821d8beb6c8de84c7ed671a373d7372c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486204"
---
# <a name="activecommand-property-ado"></a>ActiveCommand (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013

Indica el objeto [Command](command-object-ado.md) que ha creado el objeto [Recordset](recordset-object-ado.md) asociado.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **Variant** que contiene un objeto **Command**. El valor predeterminado es una referencia de objeto nula.

## <a name="remarks"></a>Comentarios

La propiedad **ActiveCommand** es de sólo lectura.

Si no se usó un objeto **Command** para crear el objeto **Recordset** actual, se devuelve una referencia de objeto **Null**.

Use esta propiedad para buscar el objeto **Command** asociado cuando solo dispone del objeto **Recordset** resultante.

