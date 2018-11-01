---
title: Usar objetos de datos ActiveX
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access proporciona tres modelos de objetos para utilizarlos en la creación, mantenimiento y la administración de las bases de datos de Access y sus datos relacionados, mediante el uso de Visual Basic.
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d7e8e7e6abeea9cca86c928760eddb990517a207
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887512"
---
# <a name="use-activex-data-objects"></a>Usar objetos de datos ActiveX

**Se aplica a**: Access 2013, Office 2013

Microsoft Access proporciona tres modelos de objetos para utilizarlos en la creación, mantenimiento y la administración de las bases de datos de Access y sus datos relacionados, mediante el uso de Visual Basic.

## <a name="microsoft-activex-data-objects-ado"></a>Objetos de datos ActiveX de Microsoft (Microsoft ActiveX Data Objects, ADO)

ADO contiene los objetos necesarios para crear, mantener y eliminar registros en un origen de datos dado.

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO Ext. DDL y seguridad (ADOX)

ADOX proporciona los objetos de lenguaje de definición de datos (DDL) necesarios para crear una nueva base de datos y los objetos que contiene además de los objetos necesarios para administrar la seguridad.

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Biblioteca de Microsoft Jet y Replication Objects 2.5 (JRO)

Debido a que los objetos ADO fueron diseñados para trabajar con muchas bases de datos además de las bases de datos Microsoft Jet, funciones específicas de Jet se incluyeron como parte de la biblioteca JRO.

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
<th><p>Característica</p></th>
<th><p>DAO</p></th>
<th><p>ADO1</p></th>
<th><p>ADOX2</p></th>
<th><p>JRO<br />
(Sólo para MDB)</p></th>
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
<td><p>Admitir ANSI92 SQL.* **</p></td>
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
<td><p>Crear nueva base de datos.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Editar propiedades de tabla existente.</p></td>
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
<td><p>Editar configuración de seguridad.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Compatibilidad con el atributo Compression para datos de la columna.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Editar almacenados, básica consultas o vistas SQL.</p></td>
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
<td><p>Compactar o codificar la base de datos.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<td><p>Actualizar la memoria caché.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>¿Hacer replicable la base de datos.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Hacer réplicas de la base de datos.</p></td>
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
<td><p>Editar propiedades de base de datos.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Crear propiedades de base de datos personalizada.</p></td>
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

\*\*\*Aunque el motor de base de datos de Access admite en parte ANSI 92 SQL, todavía no es totalmente compatible con ANSI92.

1 objeto usa **conexión** a base de datos de referencia.

Objeto usa **catálogo** 2 a base de datos de referencia.

Objeto usa **réplica** 3 a base de datos de referencia.

Objeto usa **JetEngine** 4 a base de datos de referencia.


> [!NOTE]
> A diferencia de DAO, objetos ADO y ADOX pueden realizar las acciones marcadas en bases de datos que no sean de Jet de siempre y cuando el proveedor para las bases de datos admite esa acción.


