---
title: Proveedor de persistencia de Microsoft OLE DB (proveedor de servicios ADO)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ee7f29fa12b7158f2886f908666fa485ddf291cd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484767"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a>Proveedor de persistencia de Microsoft OLE DB (proveedor de servicios ADO)


**Se aplica a**: Access 2013 | Office 2013 

El Proveedor de persistencia de Microsoft OLE DB permite guardar un objeto [Recordset](recordset-object-ado.md) en un archivo y, posteriormente, restaurar dicho objeto **Recordset** desde el archivo. Se conserva la información del esquema, los datos y los cambios pendientes.

El objeto **Recordset** se puede guardar en formato de propietario Advanced Data Table Gram (ADTG) o en el formato abierto XML (Lenguaje de marcado extensible).

## <a name="provider-keyword"></a>Palabra clave del proveedor

Para llamar a este proveedor, especifique la siguiente palabra clave y el siguiente valor en la cadena de conexión.

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a>Errores

En la aplicación se pueden detectar los errores siguientes emitidos por este proveedor.

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
<td><p>E_BADSTREAM</p></td>
<td><p>El archivo abierto no tiene un formato válido (es decir, el formato no es ADTG ni XML).</p></td>
</tr>
<tr class="even">
<td><p>E_CANTPERSISTROWSET</p></td>
<td><p>El objeto guardado <strong>Recordset</strong> tiene características que le impiden ser almacenado.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

El Proveedor de persistencia de Microsoft OLE DB no expone ninguna propiedad dinámica.

De momento, solo los objetos **Recordset** jerárquicos con parámetros no pueden ser guardados.

Para obtener más información acerca del almacenamiento persistente de objetos **Recordset**, vea [Persistencia de Recordset](more-about-recordset-persistence.md).

Cuando se utiliza una secuencia para abrir un **objeto Recordset**, debería haber parámetros no especifiquen más el parámetro *Source* del método **Open** .

