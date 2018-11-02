---
title: Propiedades dinámicas de ADO
TOCTitle: ADO dynamic properties
ms:assetid: a908bc52-2cb0-89c7-a997-2cde93477e4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249782(v=office.15)
ms:contentKeyID: 48546915
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab0d84931389aecb5bd495c884baa9163c52d4a6
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910925"
---
# <a name="ado-dynamic-properties"></a>Propiedades dinámicas de ADO

**Se aplica a**: Access 2013, Office 2013

Las propiedades dinámicas se pueden agregar a las colecciones [Properties](properties-collection-ado.md) de los objetos [Connection](connection-object-ado.md), [Command](command-object-ado.md) o [Recordset](recordset-object-ado.md). El origen de estas propiedades es un proveedor de datos, tal como el [Proveedor OLE DB para SQL Server](microsoft-ole-db-provider-for-sql-server.md), o un proveedor de servicios, tal como el [Servicio de cursores de Microsoft para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Consulte la documentación correspondiente del proveedor de datos o servicios para obtener más información acerca de una propiedad dinámica concreta.

El [Índice de propiedades dinámicas de ADO](ado-dynamic-property-index.md) proporciona una referencia cruzada entre los nombres ADO y OLE DB para cada propiedad dinámica estándar del proveedor OLE DB.

Las siguientes propiedades dinámicas son de interés especial, y también aparecen documentadas en los orígenes antes mencionados. La funcionalidad especial con ADO se documenta en los tema de Ayuda de ADO enumerados a continuación.

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Propiedad dinámica</th>
<th>Descripción</th>
</tr>
<tr class="odd">
<td><p><a href="optimize-property-dynamic-ado.md">Optimizar</a></p></td>
<td><p>Especifica si se debe crear un índice sobre este campo.</p></td>
</tr>
<tr class="even">
<td><p><a href="prompt-property-dynamic-ado.md">Prompt</a></p></td>
<td><p>Especifica si el proveedor OLE DB debe solicitar al usuario información de inicialización.</p></td>
</tr>
<tr class="odd">
<td><p><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></p></td>
<td><p>Especifica un nombre para el objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-command-property-dynamic-ado.md">Resync Command</a></p></td>
<td><p>Especifica una cadena de comando proporcionada por el usuario que el método <strong>Resync</strong> emite para actualizar los datos de la tabla especificada en la propiedad dinámica <strong>Unique Table</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></p></td>
<td><p><strong>Unique Table</strong> — especifica el nombre de la tabla base en la que se permiten actualizaciones, inserciones y eliminaciones.<br/><br/><strong>Unique Schema</strong> — especifica el esquema o el nombre del propietario de la tabla.<br/><br/><strong>Unique Catalog</strong> — especifica el catálogo o el nombre de la base de datos que contiene la tabla.</p></td>
</tr>
<tr class="even">
<td><p><a href="update-resync-property-dynamic-ado.md">Update Resync</a></p></td>
<td><p>Especifica si el método <strong>UpdateBatch</strong> es seguido por una operación implícita del método <strong>Resync</strong> y, si es así, el ámbito de esa operación.</p></td>
</tr>
</tbody>
</table>

<br/>

