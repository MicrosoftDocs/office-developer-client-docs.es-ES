---
title: Propiedad TableDefs. Count (DAO)
TOCTitle: Count Property
ms:assetid: 6e2cf3e5-524f-a643-b1dc-99a4b2bb2e63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195561(v=office.15)
ms:contentKeyID: 48545508
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6c997a437cc7a7ae1461e7308899c85dac44fbda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314269"
---
# <a name="tabledefscount-property-dao"></a>Propiedad TableDefs. Count (DAO)


**Se aplica a:** Access 2013, Office 2013

Devuelve el número de objetos de la colección especificada. Solo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . Count

*expresión* Variable que representa un objeto **TableDefs** .

## <a name="remarks"></a>Comentarios

Dado que los miembros de una colección comienzan por 0, deberá codificar siempre los bucles empezando con el miembro 0 y terminando con el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede utilizar un comando **For Each...Next**.

El valor de la propiedad **Count** nunca es Null. Si su valor es 0, indica que no hay objetos en la colección.

