---
title: TableDef.RecordCount Property (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b1d1ab4fee16a9664733c71522cb07a49dde149
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485123"
---
# <a name="tabledefrecordcount-property-dao"></a>TableDef.RecordCount Property (DAO)


**Se aplica a**: Access 2013 | Office 2013

Devuelve el número total de registros de un objeto **[TableDef](tabledef-object-dao.md)**. **Long** de solo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . RecordCount

*expresión* Variable que representa un objeto **TableDef** .

## <a name="remarks"></a>Observaciones

El valor de la propiedad **RecordCount** de un objeto **Recordset** o **TableDef** sin registros es 0.

Cuando trabaja con objetos vinculados**TableDef**, el valor de la propiedad **RecordCount** siempre es –1.

