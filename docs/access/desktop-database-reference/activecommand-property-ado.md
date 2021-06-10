---
title: Propiedad ActiveCommand (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18fa38176f7174f27b46604c6182dfbdaa422f06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281932"
---
# <a name="activecommand-property-ado"></a>Propiedad ActiveCommand (ADO)

**Se aplica a:** Access 2013, Office 2013

Indica el objeto [Command](command-object-ado.md) que ha creado el objeto [Recordset](recordset-object-ado.md) asociado.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **Variant** que contiene un objeto **Command**. El valor predeterminado es una referencia de objeto nula.

## <a name="remarks"></a>Comentarios

La propiedad **ActiveCommand** es de sólo lectura.

Si no **se usó** un objeto Command para crear el **objeto Recordset actual,** se devuelve una referencia de objeto **Null.**

Use esta propiedad para buscar el objeto **Command** asociado cuando solo dispone del objeto **Recordset** resultante.

