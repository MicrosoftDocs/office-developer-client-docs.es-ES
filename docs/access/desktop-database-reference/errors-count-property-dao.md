---
title: Propiedad Errors.Count (DAO)
TOCTitle: Count Property
ms:assetid: ad135955-3b18-4f99-66d9-aff1492df13b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821719(v=office.15)
ms:contentKeyID: 48547028
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c2cbbed2c7061b225d969dbd7554191e8db4a28a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293402"
---
# <a name="errorscount-property-dao"></a>Propiedad Errors.Count (DAO)


**Se aplica a:** Access 2013, Office 2013

Devuelve el número de objetos de la colección especificada. Solo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . Count

*expresión* Variable que representa un objeto **Errors.**

## <a name="remarks"></a>Comentarios

Dado que los miembros de una colección comienzan por 0, deberá codificar siempre los bucles empezando con el miembro 0 y terminando con el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede utilizar un comando **For Each...Next**.

El valor de la propiedad **Count** nunca es Null. Si su valor es 0, indica que no hay objetos en la colección.

