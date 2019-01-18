---
title: Uso de páginas (referencia de escritorio de la base de datos de Access)
TOCTitle: Using Pages
ms:assetid: 516fb7c2-c7a2-385b-83e7-2091c7283ea2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249261(v=office.15)
ms:contentKeyID: 48544817
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92d6185c3234a58ea9a84310291d0c37e0272535
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709407"
---
# <a name="using-pages"></a>Uso de páginas


**Se aplica a**: Access 2013, Office 2013

Utilice la propiedad **NúmeroDePáginas (PageCount)** para determinar cuántas páginas de datos hay en el objeto **Recordset**. *Las páginas* son grupos de registros cuyo tamaño es igual que el valor de la propiedad **PageSize** . Incluso aunque la última página esté incompleta porque haya menos registros que el valor de **PageSize**, cuenta como una página más en el valor **PageCount**. Si el objeto **Recordset** no admite esta propiedad, **PageCount** será -1, que significa que **PageCount** no se puede determinar.

Utilice la propiedad **PageSize** para determinar cuántos registros componen una página lógica de datos. El establecimiento de un tamaño de página permite utilizar la propiedad **AbsolutePage** para moverse al primer registro de una página determinada. Esto es útil en escenarios de servidor Web cuando se desea permitir al usuario que se desplace por los datos de las páginas para ver un número determinado de registros a la vez.

Esta propiedad se puede establecer en cualquier momento y su valor se utilizará para calcular la ubicación del primer registro de una página determinada.

Utilice la propiedad **AbsolutePage** para identificar el número de página en el que se encuentra el registro activo. De nuevo, el proveedor debe admitir la funcionalidad adecuada para que esta propiedad esté disponible.

**AbsolutePage** es de base uno y es igual a 1 cuando el registro activo es el primero del **conjunto de registros**. Configure esta propiedad para desplazarse al primer registro de una página determinada. Obtenga el número total de páginas a partir de la propiedad **NúmeroDePáginas (PageCount)**.

