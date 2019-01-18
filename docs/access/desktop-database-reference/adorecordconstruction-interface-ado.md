---
title: Interfaz ADORecordConstruction (ADO)
TOCTitle: ADORecordConstruction interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a53eb107bab0d31606dc161b9f9c910894c5bc6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712011"
---
# <a name="adorecordconstruction-interface-ado"></a>Interfaz ADORecordConstruction (ADO)


**Se aplica a**: Access 2013, Office 2013

La interfaz **ADORecordConstruction** se utiliza para construir un objeto **Record** de ADO a partir de un objeto **Row** de OLE DB en una aplicación C/C++.

Esta interfaz admite las propiedades siguientes:

## <a name="properties"></a>Propiedades

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="parentrow-property-ado.md">ParentRow</a></p></td>
<td><p>Sólo escritura.<br />
Establece el contenedor de un objeto <strong>Row</strong> de OLE DB en este objeto <strong>Record</strong> de ADO.</p></td>
</tr>
<tr class="even">
<td><p><a href="row-property-ado.md">Fila</a></p></td>
<td><p>Lectura y escritura.<br />
Obtiene o establece un objeto <strong>Row</strong> de OLE DB desde o sobre este objeto <strong>Record</strong> de ADO.</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Métodos

Ninguno.

## <a name="events"></a>Eventos

Ninguno.

## <a name="remarks"></a>Observaciones

Dado un objeto **Row** de OLE DB (pRow), la construcción de un objeto **Record** de ADO (), la construcción de un objeto **Record** de ADO (adoR), la cantidad a las tres siguientes operaciones básicas:

1.  Cree un objeto **Record** de ADO:
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  Consulte la interfaz **IADORecordConstruction** en el objeto **Record**:
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  Llamar a la **IADORecordConstruction::put\_fila** método de propiedad para establecer el objeto **Row** de OLE DB en el objeto **Record** de ADO:
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
El objeto **adoR** resultante representa ahora el objeto **Record** de ADO construido a partir del objeto **Row** de OLE DB.

Un objeto **Record** de ADO se puede crear también a partir del contenedor de un objeto **Row** de OLE DB.

## <a name="requirements"></a>Requisitos

**Versión:** ADO 2.0 y versiones posteriores

**Biblioteca:** msado15.dll

**UUID:** 00000567-0000-0010-8000-00AA006D2EA4

