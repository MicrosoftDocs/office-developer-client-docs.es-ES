---
title: Propiedad Workspaces. Count (DAO)
TOCTitle: Count Property
ms:assetid: bc7c5a11-13d3-27bd-1be4-5d069e888ac2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822719(v=office.15)
ms:contentKeyID: 48547414
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 692240130d0a5aa32899b94a18302721da01d44d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302564"
---
# <a name="workspacescount-property-dao"></a>Propiedad Workspaces. Count (DAO)


**Se aplica a:** Access 2013, Office 2013

Devuelve el número de objetos de la colección especificada. Solo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . Count

*expresión* Variable que representa un objeto **Workspaces** .

## <a name="remarks"></a>Comentarios

Dado que los miembros de una colección comienzan por 0, deberá codificar siempre los bucles empezando con el miembro 0 y terminando con el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede utilizar un comando **For Each...Next**.

El valor de la propiedad **Count** nunca es Null. Si su valor es 0, indica que no hay objetos en la colección.

