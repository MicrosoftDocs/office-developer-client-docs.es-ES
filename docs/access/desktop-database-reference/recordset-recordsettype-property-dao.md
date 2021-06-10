---
title: Propiedad Recordset.RecordsetType (DAO)
TOCTitle: RecordsetType Property
ms:assetid: a66d4043-08cc-ead1-f9ff-efc7d7ea21bf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821178(v=office.15)
ms:contentKeyID: 48546853
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13361
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 64f7dda8bec7806ef510d265deab350dc3cdad6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307633"
---
# <a name="recordsetrecordsettype-property-dao"></a>Propiedad Recordset.RecordsetType (DAO)

**Se aplica a:** Access 2013, Office 2013

Puede utilizar la propiedad **RecordsetType** para especificar el tipo de conjunto de registros que se hace disponible para un formulario. **Byte** de Lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . RecordsetType

*expression* Variable que representa un objeto **Form**.

## <a name="remarks"></a>Comentarios

La propiedad **RecordsetType** usa los siguientes valores en una base de datos de Microsoft Access.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Configuración</p></th>
<th><p>Tipo de conjunto de registros</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0</p></td>
<td><p>Dynaset</p></td>
<td><p>(Valor predeterminado) Puede modificar controles dependientes basados en una única tabla o en tablas con una relación uno a uno. Para los controles enlazados a campos basados en tablas con una relación de uno a varios, no puede editar los datos del campo de combinación en un lado de la relación a menos que se habilite la actualización en cascada entre las &quot; &quot; tablas.</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td><p>Dynaset (Actualizaciones no coherentes)</p></td>
<td><p>Se pueden editar todas las tablas y los controles vinculados a sus campos.</p></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
<td><p>Instantánea</p></td>
<td><p>No se puede editar las tablas o sus controles dependientes.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!NOTA] Si no desea que se puedan modificar los datos de controles dependientes cuando un formulario está en la vista Formulario o en la vista Hoja de datos, puede establecer la propiedad **RecordsetType** en 2.

La propiedad **RecordsetType** usa los siguientes valores en un proyecto de Microsoft Access (.ADP).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Configuración</p></th>
<th><p>Tipo de conjunto de registros</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>3</p></td>
<td><p>Instantánea</p></td>
<td><p>No se puede editar las tablas o sus controles dependientes.</p></td>
</tr>
<tr class="even">
<td><p>4 </p></td>
<td><p>Snapshot actualizable</p></td>
<td><p>(Valor predeterminado) Se pueden modificar todas las tablas y los controles dependientes de sus campos.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!NOTA] Si se modifica la propiedad **RecordsetType** de un formulario o informe abierto, se vuelve a crear automáticamente el conjunto de registros.

Puede crear formularios basados en varias tablas base con campos vinculados a los controles del formulario. Según el valor de la propiedad **RecordsetType**, podrá limitar qué control dependiente se puede editar.

Además del control de edición proporcionado por **RecordsetType**, cada control de un formulario tiene una **propiedad Locked** que puede establecer para especificar si el control y sus datos subyacentes se pueden editar. Si la propiedad **Locked** se establece en Yes, no se podrán editar los datos.

## <a name="example"></a>Ejemplo

En el siguiente ejemplo, se podrán editar los datos solo cuando la identificación del usuario sea Admin. Este ejemplo de código establece la propiedad **RecordsetType** a Snapshot si la variable pública  no es ADMIN.

```vb
    Sub Form_Open(Cancel As Integer) 
     Const conSnapshot = 2 
     If gstrUserID <> "ADMIN" Then 
     Forms!Employees.RecordsetType = conSnapshot 
     End If 
    End Sub
```

## <a name="see-also"></a>Vea también

- [Objeto Form](https://docs.microsoft.com/office/vba/api/Access.Form)


