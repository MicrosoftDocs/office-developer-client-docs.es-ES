---
title: Recordset2.MoveLast (método) (DAO)
TOCTitle: MoveLast Method
ms:assetid: 32717786-c59c-ec22-666b-fc78e4265c5a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192306(v=office.15)
ms:contentKeyID: 48544079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d5e636bf5ecae615df458754d6c4e08f00065ff
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923612"
---
# <a name="recordset2movelast-method-dao"></a>Recordset2.MoveLast (método) (DAO)


**Se aplica a**: Access 2013, Office 2013

Se desplaza al último registro de un objeto **Recordset** especificado y convierte ese registro en el registro activo.

## <a name="syntax"></a>Sintaxis

*expresión* . MoveLast (***Opciones***)

*expresión* Variable que representa un objeto **Recordset2** .

### <a name="parameters"></a>Parámetros

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
<th><p>Necesario/Opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Opciones</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Establecido en <strong>dbRunAsync</strong> para ejecutar la llamada en <strong>MoveLast</strong> de forma asincrónica.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

Utilice los métodos **Move** para desplazarse de un registro a otro sin aplicar una condición.

Si edita el registro activo, asegúrese de que utiliza el método **Update** para guardar los cambios antes de moverse a otro registro. Si se desplaza a otro registro sin ejecutar una actualización, los cambios se pierden sin advertencia.

Cuando abre un objeto **Recordset**, el primer registro es el activo y la propiedad **BOF** es **False**. Si **Recordset** no contiene registros, la propiedad **BOF** es **True** y no hay ningún registro activo.

Si el primer o el último registro ya está activo cuando utiliza **MoveFirst** o **MoveLast**, el registro activo no cambia.

Si el objeto recordset hace referencia a un **objeto Recordset** de tipo tabla (sólo áreas de trabajo de Microsoft Access), el desplazamiento sigue el índice actual. Puede definir el índice actual mediante la propiedad **Index**. Si no define el índice actual, el orden de los registros devueltos queda sin definir.


> [!NOTE]
> <P>[!NOTA] Puede usar el método <STRONG>MoveLast</STRONG> para llenar totalmente un objeto <STRONG>Recordset</STRONG> de tipo dynaset o snapshot y que proporcione el número actual de registros de <STRONG>Recordset</STRONG>. No obstante, si usa <STRONG>MoveLast</STRONG> de esta forma, puede ralentizar el rendimiento de la aplicación. Solo debe usar <STRONG>MoveLast</STRONG> para obtener el recuento de registros si es absolutamente necesario para lograr un recuento preciso en un objeto <STRONG>Recordset</STRONG> recién abierto. Si usa la constante <STRONG>dbRunAsync</STRONG> con <STRONG>MoveLast</STRONG>, la llamada al método es asincrónica. Puede usar la propiedad <STRONG>StillExecuting</STRONG> para determinar cuándo está totalmente lleno el objeto <STRONG>Recordset</STRONG> y el método <STRONG>Cancel</STRONG> para terminar la ejecución de la llamada a método <STRONG>MoveLast</STRONG> asincrónica.</P>



No puede usar los métodos **MoveFirst**, **MoveLast**ni **MovePrevious** en un objeto **Recordset** de tipo forward – only.

Para mover hacia delante o hacia atrás la posición del registro actual en un objeto **Recordset** un número determinado de registros, use el método **Move**.

