---
title: Códigos de error de DataControl
TOCTitle: DataControl error codes
ms:assetid: d81446e2-aae6-b460-08a3-eae9920dc767
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250089(v=office.15)
ms:contentKeyID: 48548027
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 387f37e180d346c09cf3dadbf66f665cb83dbd0a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707643"
---
# <a name="datacontrol-error-codes"></a>Códigos de error de DataControl


**Se aplica a**: Access 2013, Office 2013

En la tabla siguiente se enumeran los códigos de error del objeto [RDS.DataControl](datacontrol-object-rds.md). Se muestra la traducción decimal positiva de los dos bytes inferiores, la traducción decimal negativa del código de error completo y los valores hexadecimales.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Códigos de error de RDS.DataControl</p></th>
<th><p>Número</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>IDS_AsyncPending</strong></p></td>
<td><p>4107<br />
-2146824175<br />
0x800A1011</p></td>
<td><p>No se puede efectuar la operación con una operación asíncrona pendiente.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_BadInlineTablegram</strong></p></td>
<td><p>4105<br />
-2146824183<br />
0x800A1009</p></td>
<td><p>Tablegram en línea no válido.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_CantConnect</strong></p></td>
<td><p>4099<br />
-2146824189<br />
0x800A1003</p></td>
<td><p>No se puede conectar al servidor.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_CantCreateObject</strong></p></td>
<td><p>4100<br />
-2146824188<br />
0x800A1004</p></td>
<td><p>No se puede crear el objeto de negocios.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_CantFindDataspace</strong></p></td>
<td><p>4102<br />
-2146824186<br />
0x800A1006</p></td>
<td><p>La propiedad Dataspace no es válida.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_CantInvokeMethod</strong></p></td>
<td><p>4101<br />
-2146824187<br />
0x800A1005</p></td>
<td><p>No se puede invocar el método en el objeto de negocios.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_CrossDomainWarning</strong></p></td>
<td><p>4112<br />
-2146824170<br />
0x800A1016</p></td>
<td><p>Esta página obtiene acceso a datos en otro dominio. ¿Desea permitir esto? Para evitar este mensaje en Internet Explorer, puede agregar un sitio Web seguro a la zona Sitios de confianza en la ficha <strong>seguridad</strong> del cuadro de diálogo <strong>Opciones de Internet</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_InvalidADCClientVersion</strong></p></td>
<td><p>4106<br />
-2146824176<br />
0x800A1010</p></td>
<td><p>Versión de cliente de RDS no válida, El cliente es más reciente que el servidor.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_INVALIDARG</strong></p></td>
<td><p>5376<br />
-2147019520<br />
0x80071500</p></td>
<td><p>Uno o más argumentos no son válidos.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_InvalidBindings</strong></p></td>
<td><p>4097<br />
-2146824191<br />
0x800A1001</p></td>
<td><p>Error en la propiedad de enlaces.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_InvalidParam</strong></p></td>
<td><p>4110<br />
-2146824172<br />
0x800A1014</p></td>
<td><p>Uno o más argumentos no son válidos.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_NOINTERFACE</strong></p></td>
<td><p>5377<br />
-2147019519<br />
0x80071501</p></td>
<td><p>Interfaz no compatible.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_NotReentrant</strong></p></td>
<td><p>4111<br />
-2146824171<br />
0x800A1015</p></td>
<td><p>La petición no se puede ejecutar mientras el controlador de eventos esté procesando.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_ObjectNotSafe</strong></p></td>
<td><p>4103<br />
-2146824185<br />
0x800A1007</p></td>
<td><p>La configuración de seguridad de este equipo prohíbe la creación de objetos de negocio.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_RecordsetNotOpen</strong></p></td>
<td><p>4109<br />
-2146824173<br />
0x800A1013</p></td>
<td><p><strong>Recordset</strong> no abierto.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_ResetInvalidField</strong></p></td>
<td><p>4108<br />
-2146824174<br />
0x800A1012</p></td>
<td><p>La columna especificada en <strong>SortColumn</strong> o <strong>FilterColumn</strong> no existe.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_RowsetNotUpdateable</strong></p></td>
<td><p>4104<br />
-2146824184<br />
0x800A1008</p></td>
<td><p>No se puede actualizar el conjunto de filas.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_UnexpectedError</strong></p></td>
<td><p>4351<br />
-2146823937<br />
0x800A10FF</p></td>
<td><p>Error inesperado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_UpdatesFailed</strong></p></td>
<td><p>4098<br />
-2146824190<br />
0x800A1002</p></td>
<td><p>No se puede actualizar la base de datos.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_URLMONNotFound</strong></p></td>
<td><p>4119<br />
-2146824169<br />
0x800A1017</p></td>
<td><p>La propiedad <strong>URL</strong> de DataControl necesita el archivo del sistema Urlmon.dll, pero no se puede encontrar.</p></td>
</tr>
</tbody>
</table>

