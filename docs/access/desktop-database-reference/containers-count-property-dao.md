---
title: Containers.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 3b0bf865-a4d5-82bb-c1a9-9957f110db4c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192657(v=office.15)
ms:contentKeyID: 48544276
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 49ec4181d64f26d7a1a5d54ed58bfef6c1206bda
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873414"
---
# <a name="containerscount-property-dao"></a>Containers.Count Property (DAO)


**Se aplica a**: Access 2013, Office 2013

Devuelve el número de objetos **[Connection](connection-object-dao.md)** de la colección **[Connections](connections-collection-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expresión* . Recuento

*expresión* Variable que representa un objeto **Connections** .

## <a name="remarks"></a>Observaciones

Dado que los miembros de una colección comienzan por el 0, siempre debe codificar los bucles empezando por el miembro 0 y terminando por el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede usar un comando **For Each...Next**.

El valor de la propiedad **Count** nunca es Null. Si su valor es 0, no hay objetos en la colección.

