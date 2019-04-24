---
title: Count (propiedad, ADO)
TOCTitle: Count property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e2a341a82e5cdc9ed5a55ca9f4b80ba80c6875bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295474"
---
# <a name="count-property-ado"></a>Count (propiedad, ADO)


**Se aplica a:** Access 2013, Office 2013

Indica el número de objetos de una colección.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **Long**.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Count** para determinar cuántos objetos contiene una colección.

Dado que la numeración de los miembros de una colección comienza por cero, deberá codificar siempre los bucles empezando con el miembro cero y terminando con el valor de la propiedad **Count** menos 1. Si utiliza Microsoft Visual Basic y desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, utilice el comando **For** **Each...Next**.

Si la propiedad **Count** es cero, significa que no hay ningún objeto en la colección.

