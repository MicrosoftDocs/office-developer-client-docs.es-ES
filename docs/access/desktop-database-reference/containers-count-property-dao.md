---
title: Propiedad Containers.Count (DAO)
TOCTitle: Count Property
ms:assetid: 3b0bf865-a4d5-82bb-c1a9-9957f110db4c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192657(v=office.15)
ms:contentKeyID: 48544276
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0ced7b6ed0e42a17507137645fd017a6fb1a5ae3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925054"
---
# <a name="containerscount-property-dao"></a>Propiedad Containers.Count (DAO)


**Se aplica a**: Access 2013, Office 2013

Devuelve el número de objetos **[Connection](connection-object-dao.md)** de la colección **[Connections](connections-collection-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expresión* . Recuento

*expresión* Variable que representa un objeto **Connections** .

## <a name="remarks"></a>Observaciones

Dado que los miembros de una colección comienzan por el 0, siempre debe codificar los bucles empezando por el miembro 0 y terminando por el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede usar un comando **For Each...Next**.

El valor de la propiedad **Count** nunca es Null. Si su valor es 0, no hay objetos en la colección.

