---
title: CancelUpdate (método, ADO)
TOCTitle: CancelUpdate method (ADO)
ms:assetid: 2bd4d168-ba52-7786-5046-44febeda88e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249065(v=office.15)
ms:contentKeyID: 48543938
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4585679688929532d7f50be9efc71b2830bb6587
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296629"
---
# <a name="cancelupdate-method-ado"></a>CancelUpdate (método, ADO)


**Se aplica a:** Access 2013, Office 2013

Cancela los cambios realizados en la fila activa o fila nueva de un objeto [Recordset](recordset-object-ado.md), o bien, la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), antes de llamar al método [Update](update-method-ado.md).

## <a name="syntax"></a>Sintaxis

*objeto Recordset*. CancelUpdate

*registro*. *Campos*. CancelUpdate

## <a name="remarks"></a>Comentarios

**Recordset**

Utilice el método **CancelUpdate** para cancelar los cambios realizados en la fila actual o descartar una fila recién agregada. No puede cancelar los cambios realizados en la fila actual o una fila nueva después de llamar al método **Update**, a menos que los cambios formen parte de una transacción que puede deshacer con el método [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), o bien, formen parte de una actualización por lotes. En este último caso, puede cancelar el método **Update** con el método **CancelUpdate** o [CancelBatch](cancelbatch-method-ado.md).

Si está agregando una fila nueva al llamar al método **CancelUpdate**, la actual fila pasa a ser la fila que era actual antes de la llamada a [AddNew](addnew-method-ado.md).

Si está en modo de edición y desea salir del registro actual (por ejemplo, con [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) o [Close](close-method-ado.md)), puede usar **CancelUpdate** para cancelar los cambios pendientes. Quizás tenga que hacer esto si la actualización no se puede enviar correctamente al origen de datos (por ejemplo, un intento de eliminación que genera un error debido a infracciones de la integridad referencial dejará el objeto **Recordset** en modo de edición después de una llamada a [Delete](delete-method-ado-recordset.md)).

**Record**

El método **CancelUpdate** cancela todas las inserciones o eliminaciones pendientes de los objetos [Field](field-object-ado.md), además de cancelar las actualizaciones pendientes de los campos existentes y restaurar sus valores originales. La propiedad [Status](status-property-ado-recordset.md) de todos los campos de la colección **Fields** se establece en **adFieldOK**.

