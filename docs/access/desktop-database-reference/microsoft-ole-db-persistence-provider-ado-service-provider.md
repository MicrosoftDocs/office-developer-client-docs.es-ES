---
title: Proveedor de persistencia de Microsoft OLE DB (proveedor de servicios ADO)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4045445120d42f1ca88fce22ce566fc970fce28b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288956"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a>Proveedor de persistencia de Microsoft OLE DB (proveedor de servicios ADO)


**Se aplica a:** Access 2013, Office 2013 

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

Si se usa una secuencia para abrir un objeto **Recordset**, no deben especificarse más parámetros que el parámetro *Source* del método **Open**.

