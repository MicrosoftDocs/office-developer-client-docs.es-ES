---
title: Propiedad Recordsets.Count (DAO)
TOCTitle: Count Property
ms:assetid: 4362aa16-c8e9-e517-887e-c4532bd1eef9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192940(v=office.15)
ms:contentKeyID: 48544500
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a81c1ede8a3afb95e39b2c33fb8112119faf8bd8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722840"
---
# <a name="recordsetscount-property-dao"></a>Propiedad Recordsets.Count (DAO)


**Se aplica a**: Access 2013, Office 2013

Devuelve el número de objetos de la colección especificada. **Integer** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . Recuento

*expresión* Variable que representa un objeto **Recordsets** .

## <a name="remarks"></a>Observaciones

Dado que los miembros de una colección comienzan por el 0, siempre debe codificar los bucles empezando por el miembro 0 y terminando por el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede usar un comando **For Each...Next**.

El valor de la propiedad **Count** nunca es Null. Si su valor es 0, no hay objetos en la colección.

