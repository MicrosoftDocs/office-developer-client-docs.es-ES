---
title: Status (propiedad, Field de ADO)
TOCTitle: Status property (ADO Field)
ms:assetid: 7a7b45e8-2934-2e8e-77fa-a4f38272548d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249507(v=office.15)
ms:contentKeyID: 48545795
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7ba5c55e05cb8ab653a296982154bf93e1ffb08d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946261"
---
# <a name="status-property-ado-field"></a>Status (propiedad, Field de ADO)


**Se aplica a**: Access 2013, Office 2013

Indica el estado de un objeto [Field](field-object-ado.md).

## <a name="return-value"></a>Valor devuelto

Devuelve un valor [FieldStatusEnum](fieldstatusenum.md). El valor predeterminado es **adFieldOK**.

## <a name="remarks"></a>Comentarios

Esta propiedad siempre devuelve **adFieldOK** para los campos de un objeto [Recordset](recordset-object-ado.md).

Las adiciones y eliminaciones llevadas a cabo en las colecciones [Fields](fields-collection-ado.md) del objeto [Record](record-object-ado.md) se almacenan en caché hasta que se llama al método [Update](update-method-ado.md). La propiedad **Status** permite determinar qué campos se han agregado o eliminado correctamente.

Para mejorar el rendimiento, los cambios de esquema se almacenan en caché hasta que se llama a **Update** y, entonces, se llevan a cabo en una actualización optimista masiva. Si no se llama al método **Update**, el servidor no se actualiza. Si alguna actualización produce un error, se devuelve un error y la propiedad **Status** indica los valores combinados del código de estado de la operación y el error. Por ejemplo, **adFieldPendingInsert** **OR** **adFieldPermissionDenied**. La propiedad **Status** de cada objeto **Field** se puede usar para determinar el motivo por el que no se ha agregado, modificado o eliminado el objeto **Field**. **Estado** sólo forma significativa se expone en el **registro**. Colección de **campos** y no el **conjunto de registros**. Colección de **campos** .

A la hora de agregar, modificar o eliminar un objeto **Field** pueden surgir dos problemas. Si el usuario elimina un objeto **Field**, se marca para eliminación en la colección **Fields**. Si el siguiente método **Update** devuelve un error debido a que el usuario ha intentado eliminar un objeto **Field** para el que no tiene permiso, **Field** tendrá un estado **adFieldPermissionDenied** **OR** **adFieldPendingDelete**. Al llamar al método [CancelUpdate](cancelupdate-method-ado.md) se restauran los valores originales y se establece **Status** en **adFieldOK**. Del mismo modo, el método **Update** puede devolver un error debido a que se haya agregado un nuevo objeto **Field** y se le haya otorgado un valor inadecuado. En ese caso, el nuevo objeto **Field** se encontrará en la colección **Fields** y tendrá un estado **adFieldPendingInsert** y quizás **adFieldCantCreate**. Es posible proporcionar un valor adecuado para el nuevo objeto **Field** y volver a llamar a **Update**. Tenga en cuenta que llamar a **Resync** en su lugar requiere al proveedor.

