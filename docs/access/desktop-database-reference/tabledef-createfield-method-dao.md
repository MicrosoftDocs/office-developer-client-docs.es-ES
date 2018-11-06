---
title: TableDef.CreateField (método) (DAO)
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
ms.openlocfilehash: b19cf0819353dbe4d6cdb017faf0e38b3bfb7757
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997010"
---
# <a name="tabledefcreatefield-method-dao"></a><span data-ttu-id="63082-102">TableDef.CreateField (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="63082-102">TableDef.CreateField method (DAO)</span></span>

<span data-ttu-id="63082-103">**Se aplica a:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="63082-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="63082-104">Crea un nuevo objeto **[Field](field-object-dao.md)** (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="63082-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="63082-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63082-105">Syntax</span></span>

<span data-ttu-id="63082-106">*expresión* . CreateField (_**nombre**_, _**tipo**_, _**tamaño**_)</span><span class="sxs-lookup"><span data-stu-id="63082-106">*expression* .CreateField(_**Name**_, _**Type**_, _**Size**_)</span></span>

<span data-ttu-id="63082-107">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="63082-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="63082-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63082-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="63082-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="63082-109">Name</span></span></p></th>
<th><p><span data-ttu-id="63082-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="63082-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="63082-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="63082-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="63082-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="63082-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63082-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="63082-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="63082-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="63082-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="63082-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="63082-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="63082-p101">Una cadena que asigna nombres únicos al nuevo objeto <strong>Field</strong>. Consulte la propiedad <strong><a href="connection-name-property-dao.md">Name</a></strong> para obtener más detalles sobre los nombres de <strong>Field</strong> válidos.  </span><span class="sxs-lookup"><span data-stu-id="63082-p101">A String that uniquely names the new <strong>Field</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63082-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="63082-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="63082-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="63082-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="63082-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="63082-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="63082-p102">Una constante que determina el tipo de datos del nuevo objeto <strong>Field</strong>. Consulte la propiedad <strong><a href="field-type-property-dao.md">Type</a></strong> para obtener los tipos de datos válidos.  </span><span class="sxs-lookup"><span data-stu-id="63082-p102">A constant that determines the data type of the new <strong>Field</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63082-123"><em>Size</em></span><span class="sxs-lookup"><span data-stu-id="63082-123"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="63082-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="63082-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="63082-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="63082-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="63082-126">Un Integer que indica el tamaño máximo, en bytes, de un objeto <strong>Field</strong> que contiene texto.</span><span class="sxs-lookup"><span data-stu-id="63082-126">An Integer that indicates the maximum size, in bytes, of a <strong>Field</strong> object that contains text.</span></span> <span data-ttu-id="63082-127">Vea la propiedad <strong><a href="field-size-property-dao.md">Size</a></strong> para valores size válidos.</span><span class="sxs-lookup"><span data-stu-id="63082-127">See the <strong><a href="field-size-property-dao.md">Size</a></strong> property for valid size values.</span></span> <span data-ttu-id="63082-128">Este argumento se omite para campos numéricos y de ancho fijo.</span><span class="sxs-lookup"><span data-stu-id="63082-128">This argument is ignored for numeric and fixed-width fields.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="63082-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63082-129">Return value</span></span>

<span data-ttu-id="63082-130">Field</span><span class="sxs-lookup"><span data-stu-id="63082-130">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="63082-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63082-131">Remarks</span></span>

<span data-ttu-id="63082-p104">Puede utilizar el método **CreateField** para crear un nuevo campo, así como para especificar el nombre, el tipo de datos y el tamaño del campo. Si omite uno o varios de los argumentos opcionales cuando utiliza **CreateField**, puede usar la instrucción de asignación pertinente para establecer o restablecer la propiedad correspondiente antes de agregar el nuevo objeto a una colección. Después de agregar el nuevo objeto, podrá modificar algunos de sus valores, pero no todos. Vea los temas correspondientes a cada propiedad para obtener información más detallada.</span><span class="sxs-lookup"><span data-stu-id="63082-p104">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field. If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the new object, you can alter some but not all of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="63082-136">El tipo y los argumentos de tamaño se aplican sólo a objetos **Field** de un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="63082-136">The type and Size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="63082-137">Estos argumentos se omiten cuando un objeto **Field** está asociado a un objeto **Index** o **Relation**.</span><span class="sxs-lookup"><span data-stu-id="63082-137">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="63082-138">Si Name hace referencia a un objeto que ya es un miembro de la colección, se produce un error en tiempo de ejecución cuando se utiliza el método **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="63082-138">If Name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="63082-p106">Para quitar un objeto **Field** de una colección **Fields**, utilice el método **[Delete](fields-delete-method-dao.md)** en la colección. No puede eliminar un objeto **Field** desde la colección **Fields** de un objeto **TableDef** después de crear un índice que haga referencia al campo.</span><span class="sxs-lookup"><span data-stu-id="63082-p106">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection. You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

<span data-ttu-id="63082-141">**Vínculo proporcionado por** la Comunidad [UtterAccess](https://www.utteraccess.com) .</span><span class="sxs-lookup"><span data-stu-id="63082-141">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="63082-142">UtterAccess es el principal foro de ayuda y wiki sobre Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="63082-142">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="63082-143">Agregar un campo de hipervínculo a una tabla existente con DAO </span><span class="sxs-lookup"><span data-stu-id="63082-143">Adding a hyperlink field to an existing table with DAO</span></span>](https://www.utteraccess.com/wiki/index.php/adding_a_hyperlink_field_to_an_existing_table_with_dao)

## <a name="example"></a><span data-ttu-id="63082-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63082-144">Example</span></span>

<span data-ttu-id="63082-p108">En el siguiente ejemplo se muestra cómo crear un campo calculado. El método CreateField crea un campo llamado **FullName**. Después, la propiedad Expression se configura con la expresión que calcula el valor del campo.</span><span class="sxs-lookup"><span data-stu-id="63082-p108">The following example shows how to create a calculated field. The CreateField method creates a field named **FullName**. The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="63082-148">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="63082-148">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

