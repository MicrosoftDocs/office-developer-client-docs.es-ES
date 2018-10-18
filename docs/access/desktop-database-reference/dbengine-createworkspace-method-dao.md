---
title: DBEngine.CreateWorkspace Method (DAO)
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
ms.openlocfilehash: 2464426bc7178638e8ebbfc9f5b2f6d1d1b61ca2
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602590"
---
# <a name="dbenginecreateworkspace-method-dao"></a><span data-ttu-id="1cff8-102">DBEngine.CreateWorkspace Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="1cff8-102">DBEngine.CreateWorkspace Method (DAO)</span></span>


<span data-ttu-id="1cff8-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1cff8-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="1cff8-104">Crea un nuevo objeto **[Workspace](workspace-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="1cff8-104">Creates a new **[Workspace](workspace-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cff8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cff8-105">Syntax</span></span>

<span data-ttu-id="1cff8-106">*expresión* . CreateWorkspace (***nombre***, ***nombre de usuario***, ***contraseña***, ***UseType***)</span><span class="sxs-lookup"><span data-stu-id="1cff8-106">*expression* .CreateWorkspace(***Name***, ***UserName***, ***Password***, ***UseType***)</span></span>

<span data-ttu-id="1cff8-107">*expresión* Variable que representa un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="1cff8-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="1cff8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cff8-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1cff8-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="1cff8-109">Name</span></span></p></th>
<th><p><span data-ttu-id="1cff8-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="1cff8-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="1cff8-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1cff8-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="1cff8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cff8-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1cff8-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="1cff8-113">Name</span></span></p></td>
<td><p><span data-ttu-id="1cff8-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1cff8-114">Required</span></span></p></td>
<td><p><span data-ttu-id="1cff8-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="1cff8-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="1cff8-p101"><strong>String</strong> que identifica inequívocamente el nuevo objeto <strong>Workspace</strong>. Vea el tema relativo a la propiedad <strong><a href="connection-name-property-dao.md">Name</a></strong> para obtener información detallada sobre los nombres de <strong>Workspace</strong> válidos.</span><span class="sxs-lookup"><span data-stu-id="1cff8-p101">A <strong>String</strong> that uniquely names the new <strong>Workspace</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Workspace</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cff8-118">UserName</span><span class="sxs-lookup"><span data-stu-id="1cff8-118">UserName</span></span></p></td>
<td><p><span data-ttu-id="1cff8-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1cff8-119">Required</span></span></p></td>
<td><p><span data-ttu-id="1cff8-120"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="1cff8-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="1cff8-p102"><strong>String</strong> que identifica el propietario del nuevo objeto <strong>Workspace</strong>. Vea el tema relativo a la propiedad <strong>UserName</strong> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="1cff8-p102">A <strong>String</strong> that identifies the owner of the new <strong>Workspace</strong> object. See the <strong>UserName</strong> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1cff8-123">Password</span><span class="sxs-lookup"><span data-stu-id="1cff8-123">Password</span></span></p></td>
<td><p><span data-ttu-id="1cff8-124">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1cff8-124">Required</span></span></p></td>
<td><p><span data-ttu-id="1cff8-125"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="1cff8-125"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="1cff8-126">Una <strong>cadena</strong> que contiene la contraseña para el nuevo objeto de <strong>área de trabajo</strong> .</span><span class="sxs-lookup"><span data-stu-id="1cff8-126">A <strong>String</strong> containing the password for the new <strong>Workspace</strong> object.</span></span> <span data-ttu-id="1cff8-127">La contraseña puede tener hasta 20 caracteres y puede incluir cualquier carácter excepto el carácter ASCII 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1cff8-127">The password can be up to 20 characters long and can include any characters except ASCII character 0 (null).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="1cff8-p104">[!NOTA] Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos. Las contraseñas que no son seguras no contienen una combinación de estos elementos. Contraseña segura: Y6dh!et5. Contraseña no segura: House27. Use una contraseña segura que pueda recordar para no tener que anotarla.</span><span class="sxs-lookup"><span data-stu-id="1cff8-p104">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></P>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1cff8-133">UseType</span><span class="sxs-lookup"><span data-stu-id="1cff8-133">UseType</span></span></p></td>
<td><p><span data-ttu-id="1cff8-134">Opcional</span><span class="sxs-lookup"><span data-stu-id="1cff8-134">Optional</span></span></p></td>
<td><p><span data-ttu-id="1cff8-135"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1cff8-135"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1cff8-136">Uno de los valores de <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="1cff8-136">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="1cff8-137">[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="1cff8-137">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="1cff8-138">Si se establece el argumento type en <STRONG>dbUseODBC</STRONG> , se producirá un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="1cff8-138">Setting the type argument to <STRONG>dbUseODBC</STRONG> will result in a run-time error.</span></span> <span data-ttu-id="1cff8-139">Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1cff8-139">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


</td>
</tr>
</tbody>
</table>


<span data-ttu-id="1cff8-140"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="1cff8-140"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="1cff8-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cff8-141">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="1cff8-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cff8-142">Return value</span></span>
>>>>>>> <span data-ttu-id="1cff8-143">master</span><span class="sxs-lookup"><span data-stu-id="1cff8-143">master</span></span>

<span data-ttu-id="1cff8-144">Workspace</span><span class="sxs-lookup"><span data-stu-id="1cff8-144">Workspace</span></span>

## <a name="remarks"></a><span data-ttu-id="1cff8-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1cff8-145">Remarks</span></span>

<span data-ttu-id="1cff8-146">Una vez utilizado el método **CreateWorkspace** para crear un nuevo objeto **Workspace**, se inicia una sesión **Workspace** y puede hacer referencia al objeto **Workspace** en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1cff8-146">Once you use the **CreateWorkspace** method to create a new **Workspace** object, a **Workspace** session is started, and you can refer to the **Workspace** object in your application.</span></span>

<span data-ttu-id="1cff8-p106">Los objetos **Workspace** no son permanentes y no se pueden guardar en disco. Una vez creado un objeto **Workspace**, no puede modificar ninguno de los valores de sus propiedades, excepto en el caso de la propiedad **Name**, que puede modificar antes de agregar el objeto **Workspace** a la colección **[Workspaces](workspaces-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="1cff8-p106">**Workspace** objects aren't permanent, and you can't save them to disk. Once you create a **Workspace** object, you can't alter any of its property settings, except for the **Name** property, which you can modify before appending the **Workspace** object to the **[Workspaces](workspaces-collection-dao.md)** collection.</span></span>

<span data-ttu-id="1cff8-p107">No tiene que agregar el nuevo objeto **Workspace** a una colección para poder utilizarlo. Sólo debe agregar un objeto **Workspace** recién creado si necesita hacer referencia a él a través de la colección **Workspaces**.</span><span class="sxs-lookup"><span data-stu-id="1cff8-p107">You don't have to append the new **Workspace** object to a collection before you can use it. You append a newly created **Workspace** object only if you need to refer to it through the **Workspaces** collection.</span></span>

<span data-ttu-id="1cff8-151">Para quitar un objeto **Workspace** de la colección **Workspaces**, cierre todas las bases de datos y conexiones abiertas y, a continuación, utilice el método **[Close](connection-close-method-dao.md)** en el objeto **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="1cff8-151">To remove a **Workspace** object from the **Workspaces** collection, close all open databases and connections and then use the **[Close](connection-close-method-dao.md)** method on the **Workspace** object.</span></span>

## <a name="example"></a><span data-ttu-id="1cff8-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1cff8-152">Example</span></span>

<span data-ttu-id="1cff8-p108">En este ejemplo se utiliza el método **CreateWorkspace** para crear un área de trabajo de Microsoft Access. A continuación, se muestran las propiedades del área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="1cff8-p108">This example uses the **CreateWorkspace** method to createMicrosoft Access workspace. It then lists the properties of the workspace.</span></span>

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

