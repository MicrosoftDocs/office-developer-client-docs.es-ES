---
title: Determinar qué se admite
TOCTitle: Determining What is Supported
ms:assetid: 47b44dc9-e0fd-f204-0c68-e0de9247ee2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249221(v=office.15)
ms:contentKeyID: 48544602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6114dd0fa56a87b6c2e07770795ea5889ae3c44
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883634"
---
# <a name="determining-what-is-supported"></a>Determinar qué se admite


**Se aplica a**: Access 2013, Office 2013

El método **Supports** sirve para determinar si un objeto **Recordset** especificado admite un tipo determinado de funcionalidad. Tiene la sintaxis siguiente:

`boolean = recordset.Supports( CursorOptions )`

**Supports** devuelve un valor booleano que indica si el proveedor admite todas las características identificadas mediante el argumento *CursorOptions*. Puede usar el método **Supports** para determinar qué tipos de funcionalidades admite un objeto **Recordset**. Si el objeto **Recordset** admite las características cuyas constantes correspondientes están en *CursorOptions*, el método **Supports** devuelve **True**. De lo contrario, devuelve **False**.

Con el método **Supports**, puede comprobar la disponibilidad del objeto **Recordset** para agregar nuevos registros, usar marcadores, usar el método **Find**, usar el desplazamiento, usar la propiedad **Index** y realizar actualizaciones por lotes. Para consultar una lista completa de constantes y sus significados, vea [CursorOptionEnum](cursoroptionenum.md).

Aunque el método **Supports** puede devolver **True** para una funcionalidad determinada, no garantiza que el proveedor pueda ofrecer la funcionalidad en cualquier circunstancia. El método **Supports** simplemente indica si el proveedor puede admitir la funcionalidad especificada, suponiendo que se cumplen ciertas condiciones. Por ejemplo, el método **Supports** puede indicar que un objeto **Recordset** admite actualizaciones, incluso aunque el cursor se base en una unión de varias tablas (con algunas columnas que no se pueden actualizar).

