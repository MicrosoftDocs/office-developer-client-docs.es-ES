---
title: Propiedad ReadyState (RDS)
TOCTitle: ReadyState property (RDS)
ms:assetid: e7b62205-a604-ef43-2f5d-9b51b46d2b5a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250175(v=office.15)
ms:contentKeyID: 48548412
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 71dd674e90e2438c616f0973c4f9948f1b20b1f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300822"
---
# <a name="readystate-property-rds"></a>Propiedad ReadyState (RDS)

**Se aplica a:** Access 2013, Office 2013

Indica el progreso de un objeto [DataControl](datacontrol-object-rds.md) a medida que recupera datos en su objeto [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve uno de los valores siguientes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adcReadyStateLoaded</strong></p></td>
<td><p>La consulta actual se sigue ejecutando y no se ha recuperado ninguna fila. El objeto <strong>Recordset</strong> de <strong>DataControl</strong> no está disponible para ser usado.</p></td>
</tr>
<tr class="even">
<td><p><strong>adcReadyStateInteractive</strong></p></td>
<td><p>Un conjunto inicial de filas recuperadas por la consulta actual se almacenó en el objeto <strong>Recordset</strong> de <strong>DataControl</strong> y está disponible para ser usado. Las filas restantes se están recuperando.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adcReadyStateComplete</strong></p></td>
<td><p>Todas las filas recuperadas por la consulta actual han sido almacenadas en el objeto <strong>Recordset</strong> de <strong>DataControl</strong> y están disponibles para ser usadas. Este estado también existirá si se anuló una operación a causa de un error o si no se inicializó el objeto <strong>Recordset</strong>.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!NOTA] Cada archivo ejecutable del cliente que use estas constantes debe proporcionar declaraciones para ellas. Puede cortar y pegar las declaraciones de constante que desee desde el archivo Adcvbs.inc que se encuentra en la carpeta C:\Archivos de programa\Archivos comunes\System\MSADC.

## <a name="remarks"></a>Comentarios

Utilice el evento [onReadyStateChange](onreadystatechange-event-rds.md) para controlar los cambios realizados en la propiedad **ReadyState** durante una operación de consulta asincrónica. Eso es más eficaz que comprobar de forma periódica el valor de la propiedad.

Si se produce un error durante una operación asincrónica, la propiedad **ReadyState** cambia **a adcReadyStateComplete**, la propiedad [State](state-property-ado.md) cambia de **adStateExecuting** a **adStateClosed** y la propiedad [Value](value-property-ado.md) del objeto **Recordset** permanece *Nothing*.

