---
title: Propiedad Documents.Count (DAO)
TOCTitle: Count Property
ms:assetid: 3fc0b1e6-f7be-cd43-711f-5cf5763fe7f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192858(v=office.15)
ms:contentKeyID: 48544407
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053325
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: dd9cc563ecc885fca4fa0ef5829d82aa2f8bfef6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293745"
---
# <a name="documentscount-property-dao"></a>Propiedad Documents.Count (DAO)


**Se aplica a:** Access 2013, Office 2013

Devuelve el número de objetos de la colección especificada. Solo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . Recuento

*expresión* Variable que representa un **objeto Documents.**

## <a name="remarks"></a>Comentarios

Dado que los miembros de una colección comienzan por 0, deberá codificar siempre los bucles empezando con el miembro 0 y terminando con el valor de la propiedad **Count** menos 1. Si desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, puede utilizar un comando **For Each...Next**.

El valor de la propiedad **Count** nunca es Null. Si su valor es 0, indica que no hay objetos en la colección.

