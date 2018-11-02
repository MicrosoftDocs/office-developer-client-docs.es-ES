---
title: ExecuteOptions (propiedad, RDS)
TOCTitle: ExecuteOptions property (RDS)
ms:assetid: fb244cbd-9a03-9128-1373-694c9061c9da
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250285(v=office.15)
ms:contentKeyID: 48548864
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4868cc92bdb6313c581ede7442ce8f6af9fd960d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921631"
---
# <a name="executeoptions-property-rds"></a>ExecuteOptions (propiedad, RDS)


**Se aplica a**: Access 2013, Office 2013

Indica si la ejecución asincrónica está habilitada.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve uno de los valores siguientes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adcExecSync</strong></p></td>
<td><p>Ejecuta la siguiente actualización del objeto <a href="recordset-object-ado.md">Recordset</a> de forma sincrónica.</p></td>
</tr>
<tr class="even">
<td><p><strong>adcExecAsync</strong></p></td>
<td><p>Predeterminada. Ejecuta la siguiente actualización del objeto <strong>Recordset</strong> de forma asincrónica.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> [!NOTA] Cada archivo ejecutable del cliente que usa estas constantes debe proporcionar declaraciones. Puede cortar y pegar las declaraciones de constante que desee desde el archivo Adcvbs.inc que se encuentra en la carpeta C:\Archivos de programa\Archivos comunes\System\MSADC.



## <a name="remarks"></a>Comentarios

Si **ExecuteOptions** está establecida en **adcExecAsync**, ejecuta de forma asincrónica la siguiente llamada **Refresh** en el objeto [Recordset](datacontrol-object-rds.md) de **RDS.DataControl**.

Si intenta llamar a [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md) o [Recordset](recordset-sourcerecordset-properties-rds.md) mientras se ejecuta otra operación asincrónica que podría cambiar el objeto [Recordset](datacontrol-object-rds.md) de **RDS.DataControl**, se produce un error.

Si se produce un error durante una operación asincrónica, el valor [ReadyState](readystate-property-rds.md) del objeto **RDS.DataControl** cambia de **adcReadyStateLoaded** a **adcReadyStateComplete** y el valor de la propiedad **Recordset** sigue siendo *Nothing*.

