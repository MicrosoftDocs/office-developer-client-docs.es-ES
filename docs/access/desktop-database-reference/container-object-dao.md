---
title: Objeto Container (DAO)
TOCTitle: Container Object
ms:assetid: 22e487cd-e966-fe68-fff3-c680b460cbeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191764(v=office.15)
ms:contentKeyID: 48543720
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c9ebbeae35387f4fd59c39d4c20df6033edb06b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295635"
---
# <a name="container-object-dao"></a>Objeto Container (DAO)

**Se aplica a:** Access 2013, Office 2013

Un objeto **Container** agrupa juntos tipos similares de objetos **Document**.

## <a name="remarks"></a>Comentarios

Cada objeto **Database** tiene una colección **Containers** que consta de objetos **Container** integrados. Las aplicaciones pueden definir sus propios tipos de documentos y contenedores correspondientes (sólo bases de datos del motor de base de datos de Microsoft Access); no obstante, es posible que no se admitan siempre estos objetos a través de DAO.

Algunos de estos objetos **Container** están definidos por el motor de base de datos de Microsoft Access mientras que otros pueden estar definidos por otras aplicaciones. La tabla siguiente enumera el nombre de cada objeto **Container** definido por el motor de base de datos de Microsoft Access y el tipo de información que contiene.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre del contenedor</p></th>
<th><p>Contiene información sobre</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Databases</p></td>
<td><p>Bases de datos guardadas</p></td>
</tr>
<tr class="even">
<td><p>Tablas</p></td>
<td><p>Tablas y consultas guardadas</p></td>
</tr>
<tr class="odd">
<td><p>Relations</p></td>
<td><p>Relaciones guardadas</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!NOTA] No confunda los objetos **Container** enumerados en la tabla anterior con las colecciones del mismo nombre. El objeto **Container** de bases de datos hace referencia a todos los objetos de bases de datos guardados pero la colección **Databases** hace referencia sólo a los objetos de bases de datos que están abiertos en un área de trabajo en particular.

Cada objeto **Container** tiene una colección **Documents** que contiene objetos **Document** que describen instancias de objetos integrados del tipo especificado por el objeto **Container**. Normalmente, utiliza un objeto **Container** como vínculo intermediario para la información del objeto **Document**. Puede utilizar igualmente la colección **Containers** para establecer una seguridad para todos los objetos **Document** de un tipo determinado.

Con un objeto **Container** existente, puede:

- Utilizar la propiedad **Name** para devolver el nombre predefinido del objeto **Container**.

- Utilizar la propiedad **Owner** para establecer o devolver el propietario del objeto **Container**. Para establecer la propiedad **Owner**, debe tener permiso de escritura para el objeto **Container** y establecer la propiedad en el nombre de un objeto **User** o **Group** existente.

- Utilizar las propiedades **Permissions** y **UserName** para establecer permisos de acceso para el objeto **Container**; cualquier objeto **Document** creado en la colección **Documents** de un objeto **Container** hereda estos valores de permisos de acceso.

Como los objetos **Container** están integrados, no puede crear nuevos objetos **Container** o eliminar los existentes.

Para hacer referencia a un objeto **Container** en una colección mediante su número ordinal o mediante el valor de la propiedad **Name**, utilice una de las formas sintácticas siguientes:

- **Contenedores**(0)

- **Contenedores**("*nombre*")

- **Contenedores** \! \[ *nombre*\]

## <a name="example"></a>Ejemplo

En este ejemplo se enumera la colección **Containers** de la base de datos Northwind y la colección **Properties** de cada objeto **Container** de la colección.

```vb
    Sub ContainerObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim ctrLoop As Container 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Enumerate Containers collection. 
     For Each ctrLoop In .Containers 
     Debug.Print "Properties of " & ctrLoop.Name _ 
     & " container" 
     
     ' Enumerate Properties collection of each 
     ' Container object. 
     For Each prpLoop In ctrLoop.Properties 
     Debug.Print " " & prpLoop.Name _ 
     & " = " prpLoop 
     Next prpLoop 
     
     Next ctrLoop 
     
     .Close 
     End With 
     
    End Sub
```
