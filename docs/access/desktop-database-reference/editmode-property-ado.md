---
title: EditMode (propiedad, ADO)
TOCTitle: EditMode property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d7bba0af804df89bf4c8611e184928c9bf12d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293612"
---
# <a name="editmode-property-ado"></a>EditMode (propiedad, ADO)


**Se aplica a:** Access 2013, Office 2013

Indica el estado de modificación del registro actual.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor [EditModeEnum](editmodeenum.md).

## <a name="remarks"></a>Comentarios

ADO mantiene un búfer de modificación asociado al registro actual. Esta propiedad indica si se han realizado cambios en este búfer o si se ha creado un registro nuevo. Utilice la propiedad **EditMode** para determinar el estado de modificación del registro actual. Puede probar cambios pendientes si un proceso de modificación se ha interrumpido y determinar si debe utilizar el método [Update](update-method-ado.md) o [CancelUpdate](cancelupdate-method-ado.md).

Vea el método [AddNew](addnew-method-ado.md) para obtener una descripción más detallada de la propiedad **EditMode** en condiciones de modificación diferentes.

Cuando una llamada a [Delete](delete-method-ado-recordset.md) no elimina correctamente el registro o los registros en el origen de datos (debido a infracciones de integridad referencial, por ejemplo), el [objeto Recordset](recordset-object-ado.md) permanecerá en modo de edición (**EditMode** = **adEditInProgress **). Eso significa que es necesario llamar a **CancelUpdate** antes de quitar el registro actual (con [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) o [Close](close-method-ado.md), por ejemplo).


> [!NOTE]
> [!NOTA] **EditMode** puede devolver un valor válido únicamente si hay un registro actual. **EditMode** devolverá un error si [BOF o EOF](bof-eof-properties-ado.md) son True o si se ha eliminado el registro actual.


