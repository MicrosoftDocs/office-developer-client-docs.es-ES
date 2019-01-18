---
title: CancelUpdate (método, RDS)
TOCTitle: CancelUpdate method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b0c02a9ca72add763e1d3ccf62d5ede8adaecc6b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718619"
---
# <a name="cancelupdate-method-rds"></a>CancelUpdate (método, RDS)

**Se aplica a**: Access 2013, Office 2013

Cancela los cambios realizados en la fila actual o nueva de un objeto [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxis

*DataControl*. CancelUpdate

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*DataControl* |Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).|

## <a name="remarks"></a>Comentarios

El Servicio de cursor para OLE DB mantiene una copia de los valores originales y una caché de los cambios. Al llamar a **CancelUpdate**, la caché de cambios se restablece en una caché vacía y los controles enlazados se actualizan con los datos originales.

