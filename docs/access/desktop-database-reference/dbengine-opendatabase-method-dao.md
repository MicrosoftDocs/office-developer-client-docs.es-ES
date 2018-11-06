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
ms.openlocfilehash: a00c61ce4cbb9cb9d6088d521f0c2bdb3cf7f573
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998080"
---
# <a name="dbengineopendatabase-method-dao"></a>Método DBEngine.OpenDatabase (DAO)

**Se aplica a**: Access 2013, Office 2013

Abre una base de datos especificada y devuelve una referencia al objeto **[Database](database-object-dao.md)** que la representa.

## <a name="syntax"></a>Sintaxis

*expresión* . OpenDatabase (***nombre***, ***Opciones***, ***ReadOnly***, ***Conectar***)

*expresión* Variable que representa un objeto **DBEngine** .

## <a name="parameters"></a>Parámetros

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
<td><p><em>Options</em></p></td>
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

## <a name="remarks"></a>Observaciones

Puede utilizar los valores siguientes para el argumento options.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Configuración</p></th>
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

Se aplican determinadas consideraciones cuando se utiliza dbname:

- Si se refiere a una base de datos que ya está abierta para que tenga acceso a ella otro usuario, se produce un error.

- Si no se refiere a una base de datos existente o a un nombre de origen de datos ODBC válido, se produce un error.

- Si es una cadena de longitud cero ("") y *Conectar* es "ODBC;", se muestra un cuadro de diálogo lista de todos los nombres de orígenes de datos ODBC para el usuario pueda seleccionar una base de datos.

Para cerrar una base de datos y eliminar el objeto **Database** de la colección **Databases**, use el método **[Close](connection-close-method-dao.md)** del objeto.

> [!NOTE]
> [!NOTA] Cuando acceda a un origen de datos ODBC conectado a un motor de base de datos de Microsoft Access, podrá mejorar el rendimiento de la aplicación abriendo un objeto **Database** conectado al origen de datos ODBC, en lugar de vincular los objetos [TableDef](tabledef-object-dao.md) uno por uno a tablas concretas del origen de datos ODBC.


