---
title: Método Recordset.MoveLast (DAO)
TOCTitle: MoveLast method
ms:assetid: fc0f7a33-1f55-9f5b-b00d-1b81f49b1c3e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837192(v=office.15)
ms:contentKeyID: 48548881
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 79799742499e163a43d51a2d8553adcadf27b36d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284535"
---
# <a name="recordsetmovelast-method-dao"></a>Método Recordset.MoveLast (DAO)

**Se aplica a:** Access 2013, Office 2013

Se desplaza al último registro de un objeto **Recordset** especificado y convierte ese registro en el registro activo.

## <a name="syntax"></a>Sintaxis

*expresión* . MoveLast(***Options***)

*expression* Variable que representa un objeto **Recordset**.

## <a name="parameters"></a>Parameters

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Opciones</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Establecido en <strong>dbRunAsync</strong> para ejecutar la llamada en <strong>MoveLast</strong> de forma asincrónica.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Use los métodos **Move** para desplazarse de un registro a otro sin aplicar una condición.

Si edita el registro activo, asegúrese de que usa el método **Update** para guardar los cambios antes de moverse a otro registro. Si se desplaza a otro registro sin ejecutar una actualización, los cambios se pierden sin advertencia.

Cuando abre un objeto **Recordset**, el primer registro es el activo y la propiedad **BOF** es **False**. Si **Recordset** no contiene registros, la propiedad **BOF** es **True** y no hay ningún registro activo.

Si el primer o el último registro ya está activo cuando usa **MoveFirst** o **MoveLast**, el registro actual no cambia.

Si recordset hace referencia a un objeto **Recordset** de tipo de tabla (solo en áreas de trabajo de Microsoft Access), el movimiento sigue el índice actual. Puede definir el índice actual mediante la propiedad **Index**. Si no define el índice actual, el orden de los registros devueltos queda sin definir.

> [!NOTE]
> [!NOTA] Puede usar el método **MoveLast** para llenar totalmente un objeto **Recordset** de tipo dynaset o snapshot y que proporcione el número actual de registros de **Recordset**. No obstante, si usa **MoveLast** de esta forma, puede ralentizar el rendimiento de la aplicación. Solo debe usar **MoveLast** para obtener el recuento de registros si es absolutamente necesario para lograr un recuento preciso en un objeto **Recordset** recién abierto. 
> 
> Si usa la constante **dbRunAsync** con **MoveLast**, la llamada al método es asincrónica. Puede usar la propiedad **StillExecuting** para determinar cuándo está totalmente lleno el objeto **Recordset** y el método **Cancel** para terminar la ejecución de la llamada a método **MoveLast** asincrónica.

No puede usar los métodos **MoveFirst**, **MoveLast** ni **MovePrevious** en un objeto **Recordset** de tipo de solo avance.

Para mover la posición del registro actual en un objeto **Recordset** un número específico de registros hacia delante o hacia atrás, use el método **Move**.

