---
title: Usar objetos de datos de ActiveX
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access proporciona tres modelos de objetos para usar en la creación, el mantenimiento y la administración de las bases de datos de Access y sus datos relacionados mediante Visual Basic.
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3b530db43a816e66b9fbef254984142aadf0b841
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312743"
---
# <a name="use-activex-data-objects"></a>Usar objetos de datos de ActiveX

**Se aplica a:** Access 2013, Office 2013

Microsoft Access proporciona tres modelos de objetos para usar en la creación, el mantenimiento y la administración de las bases de datos de Access y sus datos relacionados mediante Visual Basic.

## <a name="microsoft-activex-data-objects-ado"></a>Objetos de datos ActiveX de Microsoft (Microsoft ActiveX Data Objects, ADO)

ADO contiene los objetos necesarios para crear, mantener y eliminar registros en un origen de datos dado.

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO ext. para DDL y seguridad (ADOX)

ADOX proporciona los objetos del lenguaje de definición de datos (DDL) necesarios para crear una nueva base de datos y sus objetos contenidos, además de los objetos necesarios para administrar la seguridad.

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Biblioteca de Microsoft Jet y Replication Objects 2.5 (JRO)

Dado que los objetos de ADO se diseñaron para funcionar con muchas bases de datos además de bases de datos de Microsoft Jet, la funcionalidad específica de Jet se desglosa en la biblioteca JRO.

En la tabla siguiente se muestran la funcionalidad que proporcionan los distintos modelos de objetos comparados con DAO.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Funcionalidad</p></th>
<th><p>DAO</p></th>
<th><p>ADO1</p></th>
<th><p>ADOX2</p></th>
<th><p>JRO<br />
(SOLO MDB)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Crear conjuntos de registros.</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Editar propiedades de inicio.</p></td>
<td><p>X</p></td>
<td><p>X**</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Compatibilidad con ANSI92 SQL.***</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Crear tablas.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Cree una nueva base de datos.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Edite las propiedades de tabla existentes.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Crear relaciones de tabla.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Editar la configuración de seguridad.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Compatibilidad con el atributo Compression para los datos de columna.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Editar vistas o consultas SQL almacenadas y básicas.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Crear consultas permanentes que son accesibles sólo mediante código.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Crear consultas accesibles por medio de la interfaz de usuario y código del contenedor de base de datos</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Base de datos compacta/codificada.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<td><p>Actualice la memoria caché.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>Hacer replicable la base de datos.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Crear réplicas de base de datos.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<td><p>Sincronizar réplicas.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Edite las propiedades de la base de datos.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Crear propiedades de base de datos personalizadas.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Editar propiedades de columna de tabla.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Sólo disponible cuando se trabaja con bases de datos Microsoft Access. Las versiones futuras del proveedor SQL pueden proporcionar estas funciones en proyectos de Microsoft Access (.adp).

\*\* Sólo disponible cuando se trabaja con proyectos de Access.

\*\*\* Aunque el motor de base de datos de Access admite algunos SQL ANSI 92, aún no es totalmente compatible con ANSI92.

1 Usa el **objeto Connection** para hacer referencia a la base de datos.

2 Usa el **objeto Catalog** para hacer referencia a la base de datos.

3 Usa el **objeto Replica** para hacer referencia a la base de datos.

4 Usa el **objeto JetEngine** para hacer referencia a la base de datos.


> [!NOTE]
> A diferencia de DAO, los objetos ADO y ADOX pueden realizar las acciones marcadas en bases de datos distintas de Jet siempre que el proveedor de dichas bases de datos admita esa acción.


