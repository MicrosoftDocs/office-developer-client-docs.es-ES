---
title: Database.CreateProperty (método) (DAO)
TOCTitle: CreateProperty Method
ms:assetid: f2039be9-5fd8-f673-dfbf-0a71540cdc98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836607(v=office.15)
ms:contentKeyID: 48548638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b0b9403c485df44935c7db5b8464d26424cf3993
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920658"
---
# <a name="databasecreateproperty-method-dao"></a><span data-ttu-id="f8ffc-102">Database.CreateProperty (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="f8ffc-102">Database.CreateProperty method (DAO)</span></span>


<span data-ttu-id="f8ffc-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8ffc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f8ffc-p101">Crea un nuevo objeto **[Property](property-object-dao.md)** definido por el usuario (solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="f8ffc-p101">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ffc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8ffc-106">Syntax</span></span>

<span data-ttu-id="f8ffc-107">*expresión* . CreateProperty (***nombre***, ***tipo***, ***valor***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="f8ffc-107">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="f8ffc-108">*expresión* Variable que representa un objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="f8ffc-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="f8ffc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8ffc-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f8ffc-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="f8ffc-110">Name</span></span></p></th>
<th><p><span data-ttu-id="f8ffc-111">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="f8ffc-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="f8ffc-112">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f8ffc-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="f8ffc-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8ffc-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8ffc-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="f8ffc-114">Name</span></span></p></td>
<td><p><span data-ttu-id="f8ffc-115">Opcional</span><span class="sxs-lookup"><span data-stu-id="f8ffc-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="f8ffc-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f8ffc-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f8ffc-p102"><strong>String</strong> que identifica inequívocamente el nuevo objeto <strong>Property</strong>. Vea el tema relativo a la propiedad <strong>Name</strong> para obtener información detallada sobre los nombres de <strong>Property</strong> válidos.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-p102">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object. See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8ffc-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="f8ffc-119">Type</span></span></p></td>
<td><p><span data-ttu-id="f8ffc-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="f8ffc-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="f8ffc-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f8ffc-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f8ffc-p103">Constante que define el tipo de datos del nuevo objeto <strong>Property</strong>. Vea el tema relativo a la propiedad <strong><a href="field-type-property-dao.md">Type</a></strong> para obtener información sobre los tipos de datos válidos.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-p103">A constant that defines the data type of the new <strong>Property</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8ffc-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f8ffc-124">Value</span></span></p></td>
<td><p><span data-ttu-id="f8ffc-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="f8ffc-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="f8ffc-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f8ffc-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f8ffc-p104"><strong>Variant</strong> que contiene el valor inicial de la propiedad. Vea el tema relativo a la propiedad <strong><a href="field-value-property-dao.md">Value</a></strong> para obtener información detallada.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-p104">A <strong>Variant</strong> containing the initial property value. See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8ffc-129">DDL</span><span class="sxs-lookup"><span data-stu-id="f8ffc-129">DDL</span></span></p></td>
<td><p><span data-ttu-id="f8ffc-130">Opcional</span><span class="sxs-lookup"><span data-stu-id="f8ffc-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="f8ffc-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f8ffc-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f8ffc-132"><strong>Variant</strong> (subtipo<strong>Boolean</strong> ) que indica si la <strong>propiedad</strong> es un objeto DDL.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-132">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="f8ffc-133">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-133">The default is False.</span></span> <span data-ttu-id="f8ffc-134">Si DDL es True, los usuarios no pueden cambiar o eliminar este objeto <strong>Property</strong> a menos que tengan un permiso dbSecWriteDef.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-134">If DDL is True, users can't change or delete this <strong>Property</strong> object unless they have dbSecWriteDef permission.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f8ffc-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8ffc-135">Return value</span></span>

<span data-ttu-id="f8ffc-136">Property</span><span class="sxs-lookup"><span data-stu-id="f8ffc-136">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="f8ffc-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8ffc-137">Remarks</span></span>

<span data-ttu-id="f8ffc-138">Solo puede crear un objeto **Property** definido por el usuario en la colección **[Properties](properties-collection-dao.md)** de un objeto que sea persistente.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-138">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="f8ffc-p106">Si omite uno o varios de los argumentos opcionales cuando utiliza **CreateProperty**, puede usar la instrucción de asignación pertinente para establecer o restablecer la propiedad correspondiente antes de agregar el nuevo objeto a una colección. Después de agregar el objeto, podrá modificar algunos de sus valores, pero no todos. Vea los temas relativos a las propiedades **Name**, **Type** y **Value** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-p106">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="f8ffc-142">Si name hace referencia a un objeto que ya es un miembro de la colección, se produce un error en tiempo de ejecución cuando se utiliza el método **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="f8ffc-142">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="f8ffc-p107">Para quitar un objeto **Property** definido por el usuario de la colección, use el método **[Delete](fields-delete-method-dao.md)** en la colección **Properties**. No se pueden eliminar propiedades integradas.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-p107">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection. You can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="f8ffc-145">Si se omite el argumento DDL, el valor predeterminado es False (no DDL).</span><span class="sxs-lookup"><span data-stu-id="f8ffc-145">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="f8ffc-146">Como no se expone ninguna propiedad DLL correspondiente, debe eliminar y volver a crear un objeto **Property** que desee cambiar de DDL a no DDL.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-146">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


## <a name="example"></a><span data-ttu-id="f8ffc-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f8ffc-147">Example</span></span>

<span data-ttu-id="f8ffc-p109">En este ejemplo se intenta establecer el valor de una propiedad definida por el usuario. Si la propiedad no existe, se utiliza el método **CreateProperty** para crear y definir el valor de la nueva propiedad. Se requiere el procedimiento SetProperty para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-p109">This example tries to set the value of a user-defined property. If the property doesn't exist, it uses the **CreateProperty** method to create and set the value of the new property. The SetProperty procedure is required for this procedure to run.</span></span>

```vb
    Sub CreatePropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Set the Archive property to True. 
       SetProperty dbsNorthwind, "Archive", True 
        
       With dbsNorthwind 
          Debug.Print "Properties of " & .Name 
           
          ' Enumerate Properties collection of the Northwind  
          ' database. 
          For Each prpLoop In .Properties 
             If prpLoop <> "" Then Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
          Next prpLoop 
     
          ' Delete the new property since this is a  
          ' demonstration. 
          .Properties.Delete "Archive" 
     
          .Close 
       End With 
     
    End Sub 
     
    Sub SetProperty(dbsTemp As Database, strName As String, _ 
       booTemp As Boolean) 
     
       Dim prpNew As Property 
       Dim errLoop As Error 
     
       ' Attempt to set the specified property. 
       On Error GoTo Err_Property 
       dbsTemp.Properties("strName") = booTemp 
       On Error GoTo 0 
     
       Exit Sub 
     
    Err_Property: 
     
       ' Error 3270 means that the property was not found. 
       If DBEngine.Errors(0).Number = 3270 Then 
          ' Create property, set its value, and append it to the  
          ' Properties collection. 
          Set prpNew = dbsTemp.CreateProperty(strName, _ 
             dbBoolean, booTemp) 
          dbsTemp.Properties.Append prpNew 
          Resume Next 
       Else 
          ' If different error has occurred, display message. 
          For Each errLoop In DBEngine.Errors 
             MsgBox "Error number: " & errLoop.Number & vbCr & _ 
                errLoop.Description 
          Next errLoop 
          End 
       End If 
     
    End Sub
```
