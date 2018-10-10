---
title: Utilizar objetos de datos ActiveX
TOCTitle: Using ActiveX Data Objects
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1f7c57ca785e115e9278145921bf50e8afe870ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484457"
---
# <a name="using-activex-data-objects"></a>Utilizar objetos de datos ActiveX


**Se aplica a**: Access 2013 | Office 2013

Microsoft Access proporciona tres modelos de objetos para utilizarlos en la creación, mantenimiento y administración de bases de datos de Access y de sus datos relacionados, mediante la utilización de Visual Basic.

## <a name="microsoft-activex-data-objects-ado"></a>Objetos de datos ActiveX de Microsoft (Microsoft ActiveX Data Objects, ADO)

ADO contiene los objetos necesarios para crear, mantener y eliminar registros en un origen de datos dado.

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO Ext. for DDL and Security (ADOX)

ADOX proporciona los objetos del lenguaje de definición de datos (Data Definition Language, DDL) necesarios para crear una nueva base de datos y los objetos que contiene además de los objetos necesarios para administrar la seguridad.

**Microsoft Jet and Replication Objects 2,5 Library (JRO)**

Puesto que los objetos ADO fueron diseñados para trabajar con muchas bases de datos además de bases de datos Microsoft Jet, las funciones específicas de Jet se incluyeron como parte de la biblioteca JRO.

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
(Sólo de Microsoft Access)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Crear conjuntos de registros</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modificar propiedades de inicio</p></td>
<td><p>X</p></td>
<td><p>X**</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Admitir ANSI92 SQL***</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Crear tablas</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Crear nueva base de datos</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modificar propiedades de tabla existente</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Crear relaciones de tablas</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modificar la configuración de seguridad</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Compatibilidad con el atributo Compression para datos de columnas</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modificar consultas o vistas SQL básicas almacenadas</p></td>
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
<td><p>Compactar o codificar la base de datos</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<td><p>Actualizar la caché</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>Hacer replicable la base de datos</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Hacer réplicas de la base de datos</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<td><p>Sincronizar réplicas</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Modificar las propiedades de base de datos</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Crear propiedades personalizadas de base de datos</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Modificar propiedades de columna de tabla</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Sólo disponible cuando se trabaja con bases de datos Microsoft Access. Las versiones futuras del proveedor SQL pueden proporcionar estas funciones en proyectos de Microsoft Access (.adp).

\*\* Sólo disponible cuando se trabaja con proyectos de Access.

\*\*\* Aunque el motor de base de datos de Access admite en parte ANSI 92 SQL, todavía no es totalmente compatible con ANSI92.

1Utiliza el objeto **Connection** para hacer referencia a la base de datos

2Utiliza el objeto **Catalog** para hacer referencia a la base de datos

3Utiliza el objeto **Replica** para hacer referencia a la base de datos

4Utiliza el objeto **JetEngine** para hacer referencia a la base de datos


> [!NOTE]
> <P>[!NOTA] A diferencia de DAO, los objetos ADO y ADOX pueden realizar las acciones marcadas en bases de datos diferentes de Jet, siempre que el proveedor de éstas admita esa acción.</P>


