---
title: Errors (colección) (ADO)
TOCTitle: Errors Collection (ADO)
ms:assetid: 76c234b8-7fec-11c5-275e-864d5d880ee7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249486(v=office.15)
ms:contentKeyID: 48545706
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fb58176e51a9e73f8551abb05636af1cfbe48d57
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875220"
---
# <a name="errors-collection-ado"></a>Errors (colección) (ADO)


**Se aplica a**: Access 2013, Office 2013

Contiene todos los objetos [Error](error-object-ado.md) creados en respuesta a un error relacionado con un único proveedor.

## <a name="remarks"></a>Comentarios

Toda operación que implique a objetos de ADO puede generar errores relacionados con el proveedor. Cuando se produce alguno de estos errores, se pueden colocar objetos **Error** en la colección **Errors** del objeto [Connection](connection-object-ado.md). Cuando otra operación ADO genera un error, se borra la colección **Errors** y el nuevo conjunto de objetos **Error** se puede colocar en la colección **Errors**.

Cada objeto **Error** representa el error de un proveedor específico, no un error de ADO. Los errores de ADO se exponen al mecanismo de control de excepciones en tiempo de ejecución. Por ejemplo, en Microsoft Visual Basic, la generación de un error específico de ADO desencadenará un evento [onError](onerror-event-rds.md) y aparecerá el objeto **Err**.

Las operaciones ADO que no generan un error no afectan a la colección **Errors**. Use el método [Clear](clear-method-ado.md) para borrar manualmente la colección **Errors**.

El conjunto de objetos **Error** de la colección **Errors** describe todos los errores que se han producido en respuesta a una única instrucción. La enumeración de los errores específicos en la colección **Errors** permite que las rutinas de tratamiento de errores determinen de forma más precisa la causa y el origen de un error, y sigan los pasos apropiados para la recuperación.

Algunos métodos y propiedades devuelven advertencias que aparecen como objetos **Error** en la colección **Errors** pero que no detienen la ejecución de un programa. Antes de llamar a los métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) o [CancelBatch](cancelbatch-method-ado.md) en un objeto [Recordset](recordset-object-ado.md), antes de llamar al método [Open](open-method-ado-connection.md) en un objeto **Connection**, o antes de establecer la propiedad [Filter](filter-property-ado.md) de un objeto **Recordset**, llame al método **Clear** en la colección **Errors**. De este modo, podrá leer la propiedad [Count](count-property-ado.md) de la colección **Errors** y comprobar si hay advertencias devueltas.


> [!NOTE]
> [!NOTA] Para obtener una explicación más detallada de cómo una única operación ADO puede generar varios errores, vea el tema sobre el objeto **Error**.


