---
title: Objeto Document (DAO)
TOCTitle: Document Object
ms:assetid: b51d4545-b157-4c7c-fdbe-16a25afffdb3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822082(v=office.15)
ms:contentKeyID: 48547247
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4dbd7de05a3bb2402d436e4bbac59f1ca4687317
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026333"
---
# <a name="document-object-dao"></a>Objeto Document (DAO)

**Se aplica a**: Access 2013, Office 2013

Un objeto **Document** incluye información sobre una instancia de un objeto. El objeto puede ser una base de datos, una tabla guardada, una consulta o una relación (sólo bases de datos del motor de base de datos de Microsoft Access).

## <a name="remarks"></a>Observaciones

Cada objeto **Container** tiene una colección **Documents** que contiene objetos **Document** que describen instancias de objetos integrados del tipo especificado por el objeto **Container**. La tabla siguiente enumera el tipo de cada objeto **Document**, el nombre de su objeto **Container** y el tipo de información que contiene **Document**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Documento</p></th>
<th><p>Contenedor</p></th>
<th><p>Contiene información sobre</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Base de datos</p></td>
<td><p>Bases de datos</p></td>
<td><p>Bases de datos guardadas</p></td>
</tr>
<tr class="even">
<td><p>Tabla o consulta</p></td>
<td><p>Tablas</p></td>
<td><p>Tabla o consulta guardada</p></td>
</tr>
<tr class="odd">
<td><p>Relación</p></td>
<td><p>Relaciones</p></td>
<td><p>Relación guardada</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!NOTA] No confunda los objetos **Container** enumerados en la tabla anterior con las colecciones del mismo nombre. El objeto **Container** de bases de datos hace referencia a todos los objetos de bases de datos guardados pero la colección **Databases** hace referencia sólo a los objetos de bases de datos que están abiertos en un área de trabajo en particular.

Con un objeto **Document**, puede:

- Utilizar la propiedad **Name** para devolver el nombre que un usuario o el motor de base de datos de Microsoft Access dieron al objeto cuando se creó.

- Usar la propiedad **Container** para devolver el nombre del objeto **Container** que contiene el objeto **Document**.

- Utilizar la propiedad **Owner** para establecer o devolver la propiedad del objeto. Para configurar la propiedad **Owner**, debe tener permiso de escritura para el objeto **Document** y establecer la propiedad en el nombre de un objeto **User** o **Group** existente.

- Usar las propiedades **UserName** o **Permissions** para establecer o devolver los permisos de acceso para un usuario o grupo para el objeto. Para configurar estas propiedades, debe tener permiso de escritura para el objeto **Document** y establecer la propiedad **UserName** en el nombre de un objeto **User** o **Group** existente.

- Utilizar las propiedades **DateCreated** y **LastUpdated** para devolver la fecha y hora en que se creó y modificó por última vez el objeto **Document**.

Dado que un objeto **Document** corresponde a un objeto existente, no se pueden crear nuevos objetos **Document** o eliminar los existentes. Para hacer referencia a un objeto **Document** en una colección mediante su número ordinal o mediante el valor de la propiedad **Name**, utilice una de las formas sintácticas siguientes:

- **Documents**(0)

- **Documentos** ("*nombre*")

- **Documentos**\!\[*nombre*\]

## <a name="example"></a>Ejemplo

En este ejemplo se enumera la colección **Documents** del contenedor Tables y, a continuación, se enumera la colección **Properties** del primer objeto **Document** de la colección.

```vb 
Sub DocumentX() 
 
 Dim dbsNorthwind As Database 
 Dim docLoop As Document 
 Dim prpLoop As Property 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind.Containers!Tables 
 Debug.Print "Documents in " & .Name & " container" 
 ' Enumerate the Documents collection of the Tables 
 ' container. 
 For Each docLoop In .Documents 
 Debug.Print " " & docLoop.Name 
 Next docLoop 
 With .Documents(0) 
 ' Enumerate the Properties collection of the first. 
 ' Document object of the Tables container. 
 Debug.Print "Properties of " & .Name & " document" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 End With 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

<br/>

En este ejemplo se utilizan las propiedades **Owner** y **SystemDB** para mostrar los propietarios de varios objetos **Document**.

```vb 
Sub OwnerX() 
 
 ' Ensure that the Microsoft Access workgroup file is 
 ' available. 
 DBEngine.SystemDB = "system.mdw" 
 
 Dim dbsNorthwind As Database 
 Dim ctrLoop As Container 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 Debug.Print "Document owners:" 
 ' Enumerate Containers collection and show the owner 
 ' of the first Document in each container's Documents 
 ' collection. 
 For Each ctrLoop In .Containers 
 With ctrLoop 
 Debug.Print " [" & .Documents(0).Name & _ 
 "] in [" & .Name & _ 
 "] container owned by [" & _ 
 .Documents(0).Owner & "]" 
 End With 
 Next ctrLoop 
 
 .Close 
 End With 
 
End Sub 
 
```

