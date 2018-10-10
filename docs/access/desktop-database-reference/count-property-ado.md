---
title: Count (propiedad, ADO)
TOCTitle: Count Property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad02d854a560e3fa99bf7454c97083e88638c520
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484937"
---
# <a name="count-property-ado"></a>Count (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013

Indica el número de objetos de una colección.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **Long**.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Count** para determinar cuántos objetos contiene una colección.

Dado que la numeración de los miembros de una colección comienza por cero, deberá codificar siempre los bucles empezando con el miembro cero y terminando con el valor de la propiedad **Count** menos 1. Si utiliza Microsoft Visual Basic y desea recorrer en bucle los miembros de una colección sin comprobar la propiedad **Count**, utilice el comando **For** **Each...Next**.

Si la propiedad **Count** es cero, significa que no hay ningún objeto en la colección.

