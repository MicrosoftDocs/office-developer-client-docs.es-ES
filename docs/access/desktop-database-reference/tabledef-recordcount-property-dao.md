---
title: Propiedad TableDef. RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5eb9588927c9e35fea54964f16150735a7374cd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314290"
---
# <a name="tabledefrecordcount-property-dao"></a>Propiedad TableDef. RecordCount (DAO)


**Se aplica a:** Access 2013, Office 2013

Devuelve el número total de registros de un objeto **[TableDef](tabledef-object-dao.md)**. **Long** de solo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . RecordCount

*expresión* Variable que representa un objeto **TableDef** .

## <a name="remarks"></a>Comentarios

Un objeto **Recordset** o **TableDef** sin registros tiene un valor 0 para la propiedad **RecordCount**.

Cuando trabaja con objetos vinculados**TableDef**, el valor de la propiedad **RecordCount** siempre es –1.

