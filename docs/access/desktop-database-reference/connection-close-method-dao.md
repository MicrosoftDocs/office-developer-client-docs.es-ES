---
title: Método Connection.Close (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bf99abf97a2eb1b88e7056a36c160eb774959719
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717219"
---
# <a name="connectionclose-method-dao"></a>Método Connection.Close (DAO)


**Se aplica a**: Access 2013, Office 2013

Cierra un objeto **Connection** abierto.

## <a name="syntax"></a>Sintaxis

*expresión* . Cerrar

*expresión* Variable que representa un objeto **Connection** .

## <a name="remarks"></a>Observaciones

Si el objeto **Recordset** ya está cerrado cuando usa **Close**, se produce un error en tiempo de ejecución.

Si intenta cerrar un objeto **Connection** mientras éste tiene objetos **Recordset** abiertos, los objetos **Recordset** se cerrarán y se cancelará cualquier actualización o modificación pendiente. De igual manera, si intenta cerrar un objeto **Workspace** mientras éste tiene objetos **Connection** abiertos, se cerrarán estos objetos **Connection**, que cerrarán a su vez sus objetos **Recordset**.

Una alternativa al método **Close** es establecer el valor de una variable de objeto en **Nothing** (Set dbsTemp = Nothing).

