---
title: Interfaz ADORecordsetConstruction (ADO)
TOCTitle: ADORecordsetConstruction Interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c7ea33eb0cdd221f0d59edfb7cd04520bb888249
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877404"
---
# <a name="adorecordsetconstruction-interface-ado"></a>Interfaz ADORecordsetConstruction (ADO)


**Se aplica a**: Access 2013, Office 2013

La interfaz **ADORecordsetConstruction** se usa para construir un objeto **Recordset** de ADO a partir de un objeto **Rowset** de OLE DB en una aplicación C/C++.

Esta interfaz admite las propiedades siguientes:

## <a name="properties"></a>Propiedades

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="chapter-property-ado.md">Capítulo</a></p></td>
<td><p>Lectura y escritura.<br />
Obtiene o establece un objeto <strong>Chapter</strong> de OLE DB desde o sobre este objeto <strong>Recordset</strong> de ADO.</p></td>
</tr>
<tr class="even">
<td><p><a href="rowposition-property-ado.md">RowPosition</a></p></td>
<td><p>Lectura y escritura.<br />
Obtiene o establece un objeto <strong>RowPosition</strong> de OLE DB desde o sobre este objeto <strong>Recordset</strong> de ADO.</p></td>
</tr>
<tr class="odd">
<td><p><a href="rowset-property-ado.md">Conjunto de filas</a></p></td>
<td><p>Lectura y escritura.<br />
Obtiene o establece un objeto <strong>Rowset</strong> de OLE DB desde o sobre este objeto <strong>Recordset</strong> de ADO.</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Métodos

Ninguno.

## <a name="events"></a>Eventos

Ninguno.

## <a name="remarks"></a>Comentarios

Dado un objeto **Rowset** de OLE DB (pRowset), la construcción de un objeto **Recordset** de ADO (), la construcción de un importe de (adoRs) del objeto **Recordset** de ADO a las tres siguientes operaciones básicas:

1. Cree un objeto **Recordset** de ADO:
    
   ```vb
    Recordset20Ptr adoRs;
    adoRs.CreateInstance(__uuidof(Recordset));
   ```
2. Consulte la interfaz **IADORecordsetConstruction** en el objeto **Recordset**:

   ```vb    
    adoRecordsetConstructionPtr adoRsConstruct=NULL;
    adoRs->QueryInterface(__uuidof(ADORecordsetConstruction),
         (void**)&adoRsConstruct);
   ```

3. Llamar a la IADORecordsetConstruction::put\_método de propiedad de conjunto de filas para establecer el objeto Rowset de OLE DB en el objeto Recordset de ADO:

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
El objeto resultante representa ahora el objeto **Recordset** de ADO construido a partir del objeto **Rowset** de OLE DB.

También se puede crear un objeto **Recordset** de ADO a partir de un objeto **Chapter** o **RowPosition** de OLE DB.

## <a name="requirements"></a>Requisitos

- **Versión:** ADO 2.0 y versiones posteriores

- **Biblioteca:** msado15.dll

- **UUID:** 00000283-0000-0010-8000-00AA006D2EA4

