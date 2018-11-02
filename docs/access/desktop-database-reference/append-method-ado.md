---
title: Append (método, ADO)
TOCTitle: Append method (ADO)
ms:assetid: cca133af-2b95-877d-0488-0d99631623f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250014(v=office.15)
ms:contentKeyID: 48547742
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 03a953b34932a5090ab40abbc7613e3518506070
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925661"
---
# <a name="append-method-ado"></a><span data-ttu-id="2bd25-102">Append (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="2bd25-102">Append method (ADO)</span></span>


<span data-ttu-id="2bd25-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2bd25-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="2bd25-p101">Anexa un objeto a una colección. Si la colección es [Fields](fields-collection-ado.md), se puede crear un nuevo objeto [Field](field-object-ado.md) antes de anexarlo a la colección.</span><span class="sxs-lookup"><span data-stu-id="2bd25-p101">Appends an object to a collection. If the collection is [Fields](fields-collection-ado.md), a new [Field](field-object-ado.md) object may be created before it is appended to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bd25-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2bd25-106">Syntax</span></span>

<span data-ttu-id="2bd25-107">*colección*. Anexar *objeto*</span><span class="sxs-lookup"><span data-stu-id="2bd25-107">*collection*.Append *object*</span></span>

<span data-ttu-id="2bd25-108">*los campos*. Anexe el *nombre*, *tipo*, *DefinedSize*, *Attrib*, *FieldValue*</span><span class="sxs-lookup"><span data-stu-id="2bd25-108">*fields*.Append *Name*, *Type*, *DefinedSize*, *Attrib*, *FieldValue*</span></span>

## <a name="parameters"></a><span data-ttu-id="2bd25-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bd25-109">Parameters</span></span>

  - <span data-ttu-id="2bd25-110">*collection*</span><span class="sxs-lookup"><span data-stu-id="2bd25-110">*collection*</span></span>

  - <span data-ttu-id="2bd25-111">Objeto de colección.</span><span class="sxs-lookup"><span data-stu-id="2bd25-111">A collection object.</span></span>

  - <span data-ttu-id="2bd25-112">*fields*</span><span class="sxs-lookup"><span data-stu-id="2bd25-112">*fields*</span></span>

  - <span data-ttu-id="2bd25-113">Colección **Fields**.</span><span class="sxs-lookup"><span data-stu-id="2bd25-113">A **Fields** collection.</span></span>

  - <span data-ttu-id="2bd25-114">*object*</span><span class="sxs-lookup"><span data-stu-id="2bd25-114">*object*</span></span>

  - <span data-ttu-id="2bd25-115">Variable de objeto que representa el objeto que se va a anexar.</span><span class="sxs-lookup"><span data-stu-id="2bd25-115">An object variable that represents the object to be appended.</span></span>

  - <span data-ttu-id="2bd25-116">*Name*</span><span class="sxs-lookup"><span data-stu-id="2bd25-116">*Name*</span></span>

  - <span data-ttu-id="2bd25-117">Valor de tipo **String** que contiene el nombre del nuevo objeto **Field**. No puede ser el nombre de ningún objeto de *fields*.</span><span class="sxs-lookup"><span data-stu-id="2bd25-117">A **String** value that contains the name of the new **Field** object, and must not be the same name as any other object in *fields*.</span></span>

  - <span data-ttu-id="2bd25-118">*Type*</span><span class="sxs-lookup"><span data-stu-id="2bd25-118">*Type*</span></span>

  - <span data-ttu-id="2bd25-p102">Valor de [DataTypeEnum](datatypeenum.md), cuyo valor predeterminado es **adEmpty**, que especifica el tipo de datos del nuevo campo. ADO no admite los siguientes tipos de datos, por lo que no deben usarse al anexar nuevos campos a un objeto **Recordset**: **adIDispatch**, **adIUnknown**, **adVariant**.</span><span class="sxs-lookup"><span data-stu-id="2bd25-p102">A [DataTypeEnum](datatypeenum.md) value, whose default value is **adEmpty**, that specifies the data type of the new field. The following data types are not supported by ADO, and should not be used when appending new fields to a **Recordset**: **adIDispatch**, **adIUnknown**, **adVariant**.</span></span>

  - <span data-ttu-id="2bd25-121">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="2bd25-121">*DefinedSize*</span></span>

  - <span data-ttu-id="2bd25-p103">Es opcional. Un valor de tipo **Long** que representa el tamaño definido, en caracteres o bytes, del nuevo campo. El valor predeterminado de este parámetro se deriva de *Type*. Campos cuyo valor de DefinedSize es mayor que 255 bytes y campos tratados como columnas de longitud variable. (No se especifica el valor predeterminado de *DefinedSize*.)</span><span class="sxs-lookup"><span data-stu-id="2bd25-p103">Optional. A **Long** value that represents the defined size, in characters or bytes, of the new field. The default value for this parameter is derived from *Type*. Fields with a DefinedSize greater than 255 bytes, and treated as variable length columns. (The default *DefinedSize* is unspecified.)</span></span>

  - <span data-ttu-id="2bd25-127">*Attrib*</span><span class="sxs-lookup"><span data-stu-id="2bd25-127">*Attrib*</span></span>

  - <span data-ttu-id="2bd25-p104">Es opcional. Un valor de [FieldAttributeEnum](fieldattributeenum.md), cuyo valor predeterminado es **adFldDefault**, que especifica los atributos del nuevo campo. Si no se especifica este valor, el campo contendrá atributos derivados de *Type*.</span><span class="sxs-lookup"><span data-stu-id="2bd25-p104">Optional. A [FieldAttributeEnum](fieldattributeenum.md) value, whose default value is **adFldDefault**, that specifies attributes for the new field. If this value is not specified, the field will contain attributes derived from *Type*.</span></span>

  - <span data-ttu-id="2bd25-131">*FieldValue*</span><span class="sxs-lookup"><span data-stu-id="2bd25-131">*FieldValue*</span></span>

  - <span data-ttu-id="2bd25-p105">Es opcional. **Variant** que representa el valor del nuevo campo. Si no se especifica, el campo se anexa con un valor null.</span><span class="sxs-lookup"><span data-stu-id="2bd25-p105">Optional. A **Variant** that represents the value for the new field. If not specified, then the field is appended with a null value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bd25-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2bd25-135">Remarks</span></span>

<span data-ttu-id="2bd25-136">**Colección Parameters**</span><span class="sxs-lookup"><span data-stu-id="2bd25-136">**Parameters Collection**</span></span>

<span data-ttu-id="2bd25-p106">Es preciso establecer el valor de la propiedad [Type](type-property-ado.md) de un objeto [Parameter](parameter-object-ado.md) antes de anexarlo a la colección **Parameters**. Si selecciona un tipo de datos de longitud variable, también deberá establecer la propiedad [Size](size-property-ado.md) en un valor mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="2bd25-p106">You must set the [Type](type-property-ado.md) property of a [Parameter](parameter-object-ado.md) object before appending it to the **Parameters** collection. If you select a variable-length data type, you must also set the [Size](size-property-ado.md) property to a value greater than zero.</span></span>

<span data-ttu-id="2bd25-p107">Describir personalmente los parámetros minimiza el número de llamadas al proveedor y, en consecuencia, mejora el rendimiento a la hora de usar procedimientos almacenados o consultas parametrizadas. Sin embargo, es preciso conocer las propiedades de los parámetros asociados a la consulta parametrizada o al procedimiento almacenado al que desee llamar.</span><span class="sxs-lookup"><span data-stu-id="2bd25-p107">Describing parameters yourself minimizes calls to the provider and consequently improves performance when using stored procedures or parameterized queries. However, you must know the properties of the parameters associated with the stored procedure or parameterized query that you want to call.</span></span>

<span data-ttu-id="2bd25-p108">Utilice el método [CreateParameter](createparameter-method-ado.md) para crear objetos **Parameter** con los valores de propiedad adecuados y utilice el método **Append** para anexarlos a la colección [Parameters](parameters-collection-ado.md). Esto le permite establecer y devolver los valores de parámetro sin tener que llamar al proveedor para obtener la información de los parámetros. Si escribe a un proveedor que no proporcione información de parámetros, debe utilizar este método para rellenar manualmente la colección **Parameters** y poder utilizar parámetros.</span><span class="sxs-lookup"><span data-stu-id="2bd25-p108">Use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the **Append** method to add them to the [Parameters](parameters-collection-ado.md) collection. This lets you set and return parameter values without having to call the provider for the parameter information. If you are writing to a provider that does not supply parameter information, you must use this method to manually populate the **Parameters** collection in order to use parameters at all.</span></span>

<span data-ttu-id="2bd25-144">**Colección Fields**</span><span class="sxs-lookup"><span data-stu-id="2bd25-144">**Fields Collection**</span></span>

<span data-ttu-id="2bd25-145">El parámetro *FieldValue* sólo es válido cuando se agrega un objeto **Field** a un objeto [Record](record-object-ado.md) , no a un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="2bd25-145">The *FieldValue* parameter is only valid when adding a **Field** object to a [Record](record-object-ado.md) object, not to a **Recordset** object.</span></span> <span data-ttu-id="2bd25-146">Con un objeto **Record**, se pueden anexar campos y proporcionar valores al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="2bd25-146">With a **Record** object, you may append fields and provide values at the same time.</span></span> <span data-ttu-id="2bd25-147">Con un objeto **Recordset**, se deben crear los campos mientras está cerrado el objeto **Recordset**, después abrir el objeto **Recordset** y asignar valores a los campos.</span><span class="sxs-lookup"><span data-stu-id="2bd25-147">With a **Recordset** object, you must create fields while the **Recordset** is closed, then open the **Recordset** and assign values to the fields.</span></span>


> [!NOTE]
> <span data-ttu-id="2bd25-p110">[!NOTA] Para los nuevos objetos **Field** que se han anexado a la colección **Fields** de un objeto **Record**, se debe establecer primero la propiedad [Value](value-property-ado.md) para que se puedan especificar las demás propiedades de **Field**. Primero, se debe asignar un valor específico a la propiedad **Value** y se debe llamar a [Update](update-method-ado.md) en la colección **Fields**. A continuación, se podrá obtener acceso a otras propiedades como [Type](type-property-ado.md) o [Attributes](attributes-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="2bd25-p110">For new **Field** objects that have been appended to the **Fields** collection of a **Record** object, the [Value](value-property-ado.md) property must be set before any other **Field** properties can be specified. First, a specific value for the **Value** property must have been assigned and [Update](update-method-ado.md) on the **Fields** collection called. Then, other properties such as [Type](type-property-ado.md) or [Attributes](attributes-property-ado.md) can be accessed.</span></span>


<span data-ttu-id="2bd25-p111">Los objetos **Field** de los siguientes tipos de datos (**DataTypeEnum**) no se pueden anexar a la colección **Fields**; si se anexan, se generará un error: **adArray**, **adChapter**, **adEmpty**, **adPropVariant** y **adUserDefined**. Además, ADO no admite los siguientes tipos de datos: **adIDispatch**, **adIUnknown** y **adIVariant**. En el caso de estos tipos, no se producirá un error cuando se anexen, pero su uso puede generar resultados imprevisibles, incluidas pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="2bd25-p111">**Field** objects of the following data types (**DataTypeEnum**) cannot be appended to the **Fields** collection and will cause an error to occur: **adArray**, **adChapter**, **adEmpty**, **adPropVariant**, and **adUserDefined**. Also, the following data types are not supported by ADO: **adIDispatch**, **adIUnknown**, and **adIVariant**. For these types, no error will occur when appended, but usage can produce unpredictable results including memory leaks.</span></span>

<span data-ttu-id="2bd25-154">**Recordset**</span><span class="sxs-lookup"><span data-stu-id="2bd25-154">**Recordset**</span></span>

<span data-ttu-id="2bd25-155">Si no se establece la propiedad [CursorLocation](cursorlocation-property-ado.md) antes de llamar al método **Append**, el valor de **CursorLocation** se establecerá automáticamente en **adUseClient** (un valor de [CursorLocationEnum](cursorlocationenum.md)) cuando se llame al método [Open](recordset-object-ado.md) del objeto [Recordset](open-method-ado-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="2bd25-155">If you do not set the [CursorLocation](cursorlocation-property-ado.md) property before calling the **Append** method, **CursorLocation** will be set to **adUseClient** (a [CursorLocationEnum](cursorlocationenum.md) value) automatically when the [Recordset](recordset-object-ado.md) object's [Open](open-method-ado-recordset.md) method is called.</span></span>

<span data-ttu-id="2bd25-p112">Se producirá un error en tiempo de ejecución si se llama al método **Append** en la colección **Fields** de un objeto **Recordset** abierto o en un objeto **Recordset** donde se ha configurado la propiedad [ActiveConnection](activeconnection-property-ado.md). Sólo se pueden anexar campos a un objeto **Recordset** que no está abierto y aún no se ha conectado a ningún origen de datos. Este suele ser el caso cuando se crea un objeto **Recordset** con el método [CreateRecordset](createrecordset-method-rds.md) o cuando se asigna a una variable de objeto.</span><span class="sxs-lookup"><span data-stu-id="2bd25-p112">A run-time error will occur if the **Append** method is called on the **Fields** collection of an open **Recordset**, or on a **Recordset** where the [ActiveConnection](activeconnection-property-ado.md) property has been set. You can only append fields to a **Recordset** that is not open and has not yet been connected to a data source. This is typically the case when a **Recordset** object is fabricated with the [CreateRecordset](createrecordset-method-rds.md) method or assigned to an object variable.</span></span>

<span data-ttu-id="2bd25-159">**Record**</span><span class="sxs-lookup"><span data-stu-id="2bd25-159">**Record**</span></span>

<span data-ttu-id="2bd25-p113">No se producirá un error en tiempo de ejecución si se llama al método **Append** en la colección **Fields** de un objeto **Record** abierto. El nuevo campo se agregará a la colección **Fields** del objeto **Record**. Si el objeto **Record** se deriva de un objeto **Recordset**, el nuevo campo no aparecerá en la colección **Fields** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2bd25-p113">A run-time error will not occur if the **Append** method is called on the **Fields** collection of an open **Record**. The new field will be added to the **Record** object's **Fields** collection. If the **Record** was derived from a **Recordset**, then the new field will not appear in the **Recordset** object's **Fields** collection.</span></span>

<span data-ttu-id="2bd25-p114">Se puede crear un campo inexistente y anexarlo a la colección **Fields** mediante la asignación de un valor al objeto de campo como si ya existiese en la colección. La asignación hará que se cree y se anexe automáticamente el objeto **Field** y, a continuación, se completa la asignación.</span><span class="sxs-lookup"><span data-stu-id="2bd25-p114">A non-existent field can be created and appended to the **Fields** collection by assigning a value to the field object as if it already existed in the collection. The assignment will trigger the automatic creation and appending of the **Field** object, then the assignment will be completed.</span></span>

<span data-ttu-id="2bd25-165">Después de anexar un objeto **Field** a la colección **Fields** de un objeto **Record**, llame al método **Update** de la colección **Fields** para guardar el cambio.</span><span class="sxs-lookup"><span data-stu-id="2bd25-165">After appending a **Field** to a **Record** object's **Fields** collection, call the **Update** method of the **Fields** collection to save the change.</span></span>

