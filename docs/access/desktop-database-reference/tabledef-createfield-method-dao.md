---
title: Método TableDef.CreateField (DAO)
TOCTitle: CreateField Method
ms:assetid: a83d797f-ea42-4a07-dd9e-b254755f0891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821396(v=office.15)
ms:contentKeyID: 48546897
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052971
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1fd66910a3630d8968f75c5a59bb535520419994
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606986"
---
# <a name="tabledefcreatefield-method-dao"></a><span data-ttu-id="18a3f-102">Método TableDef.CreateField (DAO)</span><span class="sxs-lookup"><span data-stu-id="18a3f-102">TableDef.CreateField Method (DAO)</span></span>

<span data-ttu-id="18a3f-103">**Se aplica a:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="18a3f-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="18a3f-104">Crea un nuevo objeto **[Field](field-object-dao.md)** (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="18a3f-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="18a3f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18a3f-105">Syntax</span></span>

<span data-ttu-id="18a3f-106">*expresión* . CreateField (_**nombre**_, _**tipo**_, _**tamaño**_)</span><span class="sxs-lookup"><span data-stu-id="18a3f-106">*expression* .CreateField(_**Name**_, _**Type**_, _**Size**_)</span></span>

<span data-ttu-id="18a3f-107">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="18a3f-107">*expression* A variable that represents a **TableDef** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="18a3f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18a3f-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18a3f-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="18a3f-109">Name</span></span></p></th>
<th><p><span data-ttu-id="18a3f-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="18a3f-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="18a3f-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="18a3f-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="18a3f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="18a3f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18a3f-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="18a3f-113">Name</span></span></p></td>
<td><p><span data-ttu-id="18a3f-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="18a3f-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="18a3f-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="18a3f-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="18a3f-p101">Una cadena que asigna nombres únicos al nuevo objeto <strong>Field</strong>. Consulte la propiedad <strong><a href="connection-name-property-dao.md">Name</a></strong> para obtener más detalles sobre los nombres de <strong>Field</strong> válidos.  </span><span class="sxs-lookup"><span data-stu-id="18a3f-p101">A String that uniquely names the new <strong>Field</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18a3f-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="18a3f-118">Type</span></span></p></td>
<td><p><span data-ttu-id="18a3f-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="18a3f-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="18a3f-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="18a3f-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="18a3f-p102">Una constante que determina el tipo de datos del nuevo objeto <strong>Field</strong>. Consulte la propiedad <strong><a href="field-type-property-dao.md">Type</a></strong> para obtener los tipos de datos válidos.  </span><span class="sxs-lookup"><span data-stu-id="18a3f-p102">A constant that determines the data type of the new <strong>Field</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18a3f-123">Size</span><span class="sxs-lookup"><span data-stu-id="18a3f-123">Size</span></span></p></td>
<td><p><span data-ttu-id="18a3f-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="18a3f-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="18a3f-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="18a3f-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="18a3f-126">Un Integer que indica el tamaño máximo, en bytes, de un objeto <strong>Field</strong> que contiene texto.</span><span class="sxs-lookup"><span data-stu-id="18a3f-126">An Integer that indicates the maximum size, in bytes, of a <strong>Field</strong> object that contains text.</span></span> <span data-ttu-id="18a3f-127">Vea la propiedad <strong><a href="field-size-property-dao.md">Size</a></strong> para valores size válidos.</span><span class="sxs-lookup"><span data-stu-id="18a3f-127">See the <strong><a href="field-size-property-dao.md">Size</a></strong> property for valid size values.</span></span> <span data-ttu-id="18a3f-128">Este argumento se omite para campos numéricos y de ancho fijo.</span><span class="sxs-lookup"><span data-stu-id="18a3f-128">This argument is ignored for numeric and fixed-width fields.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="18a3f-129"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="18a3f-129"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="18a3f-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18a3f-130">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="18a3f-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18a3f-131">Return value</span></span>
>>>>>>> <span data-ttu-id="18a3f-132">master</span><span class="sxs-lookup"><span data-stu-id="18a3f-132">master</span></span>

<span data-ttu-id="18a3f-133">Field</span><span class="sxs-lookup"><span data-stu-id="18a3f-133">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="18a3f-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18a3f-134">Remarks</span></span>

<span data-ttu-id="18a3f-p104">Puede utilizar el método **CreateField** para crear un nuevo campo, así como para especificar el nombre, el tipo de datos y el tamaño del campo. Si omite uno o varios de los argumentos opcionales cuando utiliza **CreateField**, puede usar la instrucción de asignación pertinente para establecer o restablecer la propiedad correspondiente antes de agregar el nuevo objeto a una colección. Después de agregar el nuevo objeto, podrá modificar algunos de sus valores, pero no todos. Vea los temas correspondientes a cada propiedad para obtener información más detallada.</span><span class="sxs-lookup"><span data-stu-id="18a3f-p104">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field. If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the new object, you can alter some but not all of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="18a3f-139">El tipo y los argumentos de tamaño se aplican sólo a objetos **Field** de un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="18a3f-139">The type and Size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="18a3f-140">Estos argumentos se omiten cuando un objeto **Field** está asociado a un objeto **Index** o **Relation**.</span><span class="sxs-lookup"><span data-stu-id="18a3f-140">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="18a3f-141">Si Name hace referencia a un objeto que ya es un miembro de la colección, se produce un error en tiempo de ejecución cuando se utiliza el método **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="18a3f-141">If Name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="18a3f-p106">Para quitar un objeto **Field** de una colección **Fields**, utilice el método **[Delete](fields-delete-method-dao.md)** en la colección. No puede eliminar un objeto **Field** desde la colección **Fields** de un objeto **TableDef** después de crear un índice que haga referencia al campo.</span><span class="sxs-lookup"><span data-stu-id="18a3f-p106">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection. You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

<span data-ttu-id="18a3f-144">**Vínculo proporcionado por** la Comunidad [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="18a3f-144">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="18a3f-145">UtterAccess es el principal foro de ayuda y wiki sobre Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="18a3f-145">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="18a3f-146">Agregar un campo de hipervínculo a una tabla existente con DAO </span><span class="sxs-lookup"><span data-stu-id="18a3f-146">Adding a hyperlink field to an existing table with DAO</span></span>](https://www.utteraccess.com/wiki/index.php/adding_a_hyperlink_field_to_an_existing_table_with_dao)

## <a name="example"></a><span data-ttu-id="18a3f-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="18a3f-147">Example</span></span>

<span data-ttu-id="18a3f-p108">En el siguiente ejemplo se muestra cómo crear un campo calculado. El método CreateField crea un campo llamado **FullName**. Después, la propiedad Expression se configura con la expresión que calcula el valor del campo.</span><span class="sxs-lookup"><span data-stu-id="18a3f-p108">The following example shows how to create a calculated field. The CreateField method creates a field named **FullName**. The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="18a3f-151">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="18a3f-151">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```

