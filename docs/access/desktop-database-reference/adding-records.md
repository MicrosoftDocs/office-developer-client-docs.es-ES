---
title: Adición de registros (referencia de base de datos de escritorio de Access)
TOCTitle: Adding records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 268cd381cdeef11f2a6f351160d930e4b169cfbf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280290"
---
# <a name="adding-records"></a>Adición de registros

**Se aplica a:** Access 2013, Office 2013

Utilice el método **AddNew** para crear e inicializar un registro nuevo en un **conjunto de registros** existente. Puede utilizar el método **Supports** con un valor **CursorOptionEnum** de **adAddNew** para comprobar si puede agregar registros al objeto **Recordset** activo.

Después de llamar al método **AddNew**, el registro nuevo pasa a ser el registro actual y sigue siéndolo después de llamar al método **Update**. Si el objeto **Recordset** no admite marcadores, tal vez no tenga acceso al registro nuevo cuando se haya movido a otro registro. Por lo tanto, dependiendo de su tipo de cursor, es posible que tenga que llamar al método **Requery** para poder tener acceso al registro nuevo.

Si llama a **AddNew** mientras modifica el registro actual o agrega un registro nuevo, ADO llamará al método **Update** para guardar todos los cambios y, después, ADO creará el registro nuevo.

Esta sección incluye los siguientes temas:

- [Adición de varios campos](adding-multiple-fields.md)
- [Determinación del modo de edición](determining-edit-mode.md)
- [Uso de AddNew en los modos Inmediato y Lote](using-addnew-in-immediate-and-batch-modes.md)

