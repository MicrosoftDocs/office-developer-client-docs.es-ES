---
title: Método DBEngine.OpenDatabase (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: 49fca321-5955-3e69-64ea-da191536eadb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193474(v=office.15)
ms:contentKeyID: 48544654
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052979
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 1cd4188931999284a6454064a0906b64cf1f519a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294256"
---
# <a name="dbengineopendatabase-method-dao"></a>Método DBEngine.OpenDatabase (DAO)

**Se aplica a:** Access 2013, Office 2013

Abre una base de datos determinada y devuelve una referencia al objeto **[Database](database-object-dao.md)** que lo representa.

## <a name="syntax"></a>Sintaxis

*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)

*expression* Variable que representa un objeto **DBEngine**.

## <a name="parameters"></a>Parameters

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p>El nombre de un archivo de base de datos de Microsoft Access existente, o el nombre de origen de datos (DSN) de un origen de datos ODBC. Para más información sobre la configuración de este valor, consulte la propiedad <strong><a href="connection-name-property-dao.md">Name</a></strong>.  </p></td>
</tr>
<tr class="even">
<td><p><em>Opciones</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Establece varias opciones para la base de datos, tal como se especifica en Comentarios.</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>True</strong> si quiere abrir la base de datos con un acceso de solo lectura o <strong>False</strong> (opción predeterminada) si quiere abrir la base de datos con un acceso de escritura/lectura.</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Especifica diversa información de conexión, incluidas las contraseñas.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor devuelto

Base de datos

## <a name="remarks"></a>Comentarios

Puede utilizar los valores siguientes para el argumento opciones.

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
<td><p><strong>True</strong></p></td>
<td><p>Abre la base de datos en modo exclusivo.</p></td>
</tr>
<tr class="even">
<td><p><strong>False</strong></p></td>
<td><p>(Opción predeterminada) Abre la base de datos en modo compartido.</p></td>
</tr>
</tbody>
</table>


Al abrir una base de datos, se agrega automáticamente a la colección **Databases**.

Al usar dbname, debe tener en cuenta ciertos aspectos:

- Si hace referencia a una base de datos que ya está abierta para que acceda otro usuario, se producirá un error.

- Si no se refiere a una base de datos existente o a un nombre de origen de datos ODBC válido, se produce un error.

- Si es una cadena de longitud cero ("") y *connect* es "ODBC;", se mostrará un cuadro de diálogo con una lista de todos los nombres de orígenes de datos ODBC registrados para que el usuario pueda seleccionar una base de datos.

Para cerrar una base de datos y eliminar el objeto **Database** de la colección **Databases**, use el método **[Close](connection-close-method-dao.md)** del objeto.

> [!NOTE]
> Cuando acceda a un origen de datos ODBC conectado a un motor de base de datos de Microsoft Access, podrá mejorar el rendimiento de la aplicación abriendo un objeto **Database** conectado al origen de datos ODBC, en lugar de vincular los objetos [TableDef](tabledef-object-dao.md) uno por uno a tablas concretas del origen de datos ODBC.


