---
title: Método DBEngine. CreateWorkspace (DAO)
TOCTitle: CreateWorkspace Method
ms:assetid: a7d73771-9420-0448-99e6-d6c4aa78683a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821374(v=office.15)
ms:contentKeyID: 48546888
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052966
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9cd84b6b5441edda2042ce0a63ae25b2cf399bd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294354"
---
# <a name="dbenginecreateworkspace-method-dao"></a>Método DBEngine. CreateWorkspace (DAO)

**Se aplica a:** Access 2013, Office 2013

Crea un nuevo objeto **[Workspace](workspace-object-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expresión* . CreateWorkspace (***nombre***, nombre de ***usuario***, ***contraseña***, ***UseType***)

*expresión* Variable que representa un objeto **DBEngine** .

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
<td><p><strong>String</strong> que identifica inequívocamente el nuevo objeto <strong>Workspace</strong>. Vea la propiedad <strong><a href="connection-name-property-dao.md">Name</a></strong> para obtener más información sobre nombres de <strong>área de trabajo</strong> válidos.</p></td>
</tr>
<tr class="even">
<td><p><em>UserName</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p><strong>String</strong> que identifica el propietario del nuevo objeto <strong>Workspace</strong>. Vea el tema relativo a la propiedad <strong>UserName</strong> para obtener más información.</p></td>
</tr>
<tr class="odd">
<td><p><em>Password</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Una <strong>cadena</strong> que contiene la contraseña para el nuevo objeto <strong>Workspace</strong> . La contraseña puede tener una longitud de hasta 20 caracteres y puede incluir cualquier carácter excepto el carácter ASCII 0 (NULL).</p>
<p><strong>Nota</strong>: Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos. Las contraseñas débiles no combinan estos elementos. Un ejemplo de contraseña segura es: Y6dh!et5. Contraseña no segura: House27. Use una contraseña segura que pueda recordar para no tener que anotarla.</p>
</td>
</tr>
<tr class="even">
<td><p><em>UseType</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uno de los valores de <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</p>
<p><strong>Nota</strong>: no se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor devuelto

Workspace

## <a name="remarks"></a>Comentarios

Una vez utilizado el método **CreateWorkspace** para crear un nuevo objeto **Workspace**, se inicia una sesión **Workspace** y puede hacer referencia al objeto **Workspace** en la aplicación.

Los objetos **Workspace** no son permanentes y no se pueden guardar en disco. Una vez creado un objeto **Workspace**, no puede modificar ninguno de los valores de sus propiedades, excepto en el caso de la propiedad **Name**, que puede modificar antes de agregar el objeto **Workspace** a la colección **[Workspaces](workspaces-collection-dao.md)**.

No tiene que agregar el nuevo objeto **Workspace** a una colección para poder utilizarlo. Sólo debe agregar un objeto **Workspace** recién creado si necesita hacer referencia a él a través de la colección **Workspaces**.

Para quitar un objeto **Workspace** de la colección **Workspaces**, cierre todas las bases de datos y conexiones abiertas y, a continuación, utilice el método **[Close](connection-close-method-dao.md)** en el objeto **Workspace**.

## <a name="example"></a>Ejemplo

En este ejemplo se utiliza el método **CreateWorkspace** para crear un área de trabajo de Microsoft Access. A continuación, se muestran las propiedades del área de trabajo.

```vb 
Sub CreateWorkspaceX() 
 
   Dim wrkAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
   DefaultType = dbUseJet 
   ' Create an unnamed Workspace object of the type  
   ' specified by the DefaultType property of DBEngine  
   ' (dbUseJet). 
   Set wrkAcc = CreateWorkspace("", "admin", "") 
 
   ' Enumerate Workspaces collection. 
   Debug.Print "Workspace objects in Workspaces collection:" 
   For Each wrkLoop In Workspaces 
      Debug.Print "  " & wrkLoop.Name 
   Next wrkLoop 
 
   With wrkAcc 
      ' Enumerate Properties collection of Microsoft Access  
      ' workspace. 
      Debug.Print _ 
         "Properties of unnamed Microsoft Access workspace" 
      On Error Resume Next 
      For Each prpLoop In .Properties 
         Debug.Print "  " & prpLoop.Name & " = " & prpLoop 
      Next prpLoop 
      On Error GoTo 0 
   End With 
 
   wrkAcc.Close 
 
End Sub 
 
```

