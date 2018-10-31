---
title: FetchOptions (propiedad, RDS)
TOCTitle: FetchOptions Property (RDS)
ms:assetid: 0d86c5e4-9abc-5c0e-dc04-4183f4c278cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248856(v=office.15)
ms:contentKeyID: 48543221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3e7251ba50b003b37cdeb0dd70fe4a98821d4c9
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861936"
---
# <a name="fetchoptions-property-rds"></a>FetchOptions (propiedad, RDS)


**Se aplica a**: Access 2013 | Office 2013

Indica el tipo de obtención asincrónica.

## <a name="setting-and-return-values"></a>Configuración y valores devueltos

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
<td><p><strong>adcFetchUpFront</strong></p></td>
<td><p>Se recuperan todos los registros del objeto <a href="recordset-object-ado.md">Recordset</a> antes de que se devuelva el control a la aplicación. El objeto completo <strong>Recordset</strong> se recupera antes de que se permita a la aplicación hacer nada con él.</p></td>
</tr>
<tr class="even">
<td><p><strong>adcFetchBackground</strong></p></td>
<td><p>El control puede volver a la aplicación en cuanto se haya recuperado el primer lote de registros. Una posterior lectura del objeto <strong>Recordset</strong> que intente obtener acceso a un registro no recuperado en el primer lote, se retrasará hasta que se recupere realmente el registro buscado, momento en que el control volverá a la aplicación.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adcFetchAsync</strong></p></td>
<td><p>Predeterminada. El control vuelve inmediatamente a la aplicación mientras los registros se recuperan en segundo plano. Si la aplicación intenta leer un registro que aún no se ha recuperado, se leerá el registro más cercano al buscado y el control volverá inmediatamente, lo que indica que se ha alcanzado el fin actual del objeto <strong>Recordset</strong>. Por ejemplo, una llamada a <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> moverá la posición actual del registro al último registro realmente recuperado, aunque haya más registros en el objeto <strong>Recordset</strong>.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> [!NOTA] Cada archivo ejecutable del cliente que use estas constantes debe proporcionar declaraciones para ellas. Puede cortar y pegar las declaraciones de constante que desee desde el archivo Adcvbs.inc que se encuentra en la carpeta C:\Archivos de programa\Archivos comunes\System\MSADC.



## <a name="remarks"></a>Comentarios

<<<<<<< HEAD en una aplicación Web, normalmente deseará utilizar **adcFetchAsync** (el valor predeterminado), ya que proporciona un mejor rendimiento. En una aplicación cliente compilada, normalmente deseará utilizar **adcFetchBackground**.
=== En una aplicación web, normalmente deseará utilizar **adcFetchAsync** (el valor predeterminado), ya que proporciona un mejor rendimiento. En una aplicación cliente compilada, normalmente deseará utilizar **adcFetchBackground**.
>>>>>>> master

