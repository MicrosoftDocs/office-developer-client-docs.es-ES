---
title: Propiedad Databases.Count (DAO)
TOCTitle: Count Property
ms:assetid: 7c542b17-9806-e00e-8cbd-58d6d17e98c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196364(v=office.15)
ms:contentKeyID: 48545831
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dbdaad343e1c149ea1f30b5c2d360cbd7bd6f1d8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927651"
---
# <a name="databasescount-property-dao"></a>Propiedad Databases.Count (DAO)


**Se aplica a**: Access 2013, Office 2013

Devuelve el número de objetos de la colección especificada. Es de solo lectura

## <a name="syntax"></a>Sintaxis

*expresión* . Recuento

*expresión* Variable que representa un objeto de **las bases de datos** .

## <a name="remarks"></a>Observaciones

Dado que los miembros de una colección comienzan por el 0, siempre debe codificar los bucles empezando por el miembro 0 y terminando por el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede usar un comando **For Each...Next**.

El valor de la propiedad **Count** nunca es Null. Si su valor es 0, no hay objetos en la colección.

