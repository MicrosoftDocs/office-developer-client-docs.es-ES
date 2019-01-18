---
title: Determinación de lo que es compatible
TOCTitle: Determining what is supported
ms:assetid: 47b44dc9-e0fd-f204-0c68-e0de9247ee2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249221(v=office.15)
ms:contentKeyID: 48544602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3abef84f05ad279edba1fcc753f0b412a807a7b9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712697"
---
# <a name="determining-what-is-supported"></a>Determinación de lo que es compatible

**Se aplica a**: Access 2013, Office 2013

El método **Supports** sirve para determinar si un objeto **Recordset** especificado admite un tipo determinado de funcionalidad. Tiene la sintaxis siguiente:

`boolean = recordset.Supports( CursorOptions )`

**Supports** devuelve un valor booleano que indica si el proveedor admite todas las características identificadas mediante el argumento *CursorOptions*. Puede usar el método **Supports** para determinar qué tipos de funcionalidades admite un objeto **Recordset**. Si el objeto **Recordset** admite las características cuyas constantes correspondientes están en *CursorOptions*, el método **Supports** devuelve **True**. De lo contrario, devuelve **False**.

Con el método **Supports**, puede comprobar la disponibilidad del objeto **Recordset** para agregar nuevos registros, usar marcadores, usar el método **Find**, usar el desplazamiento, usar la propiedad **Index** y realizar actualizaciones por lotes. Para consultar una lista completa de constantes y sus significados, vea [CursorOptionEnum](cursoroptionenum.md).

Aunque el método **Supports** puede devolver **True** para una funcionalidad determinada, no garantiza que el proveedor pueda ofrecer la funcionalidad en cualquier circunstancia. El método **Supports** simplemente indica si el proveedor puede admitir la funcionalidad especificada, suponiendo que se cumplen ciertas condiciones. Por ejemplo, el método **Supports** puede indicar que un objeto **Recordset** admite actualizaciones, incluso aunque el cursor se base en una unión de varias tablas (con algunas columnas que no se pueden actualizar).

