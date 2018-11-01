---
title: Fields.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 574de1db-2640-159b-7756-28c37acc9f83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194261(v=office.15)
ms:contentKeyID: 48544969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2f788b726f5be7cdfd7531d4522b6c653744d1c8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886749"
---
# <a name="fieldscount-property-dao"></a>Fields.Count Property (DAO)


**Se aplica a**: Access 2013, Office 2013

Devuelve el número de objetos de la colección especificada. **Integer** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . Recuento

*expresión* Variable que representa un objeto **Fields** .

## <a name="remarks"></a>Observaciones

Dado que los miembros de una colección comienzan por el 0, siempre debe codificar los bucles empezando por el miembro 0 y terminando por el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede usar un comando **For Each...Next**.

El valor de la propiedad **Count** nunca es Null. Si su valor es 0, no hay objetos en la colección.

