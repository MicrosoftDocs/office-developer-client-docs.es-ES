---
title: AddNew (método, ADO)
TOCTitle: AddNew method (ADO)
ms:assetid: bae09be0-5707-4f38-9c74-0acd0f29dbac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249899(v=office.15)
ms:contentKeyID: 48547384
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 379aa71ad875213ab8c1ae022f7c8af3350b2662
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927749"
---
# <a name="addnew-method-ado"></a><span data-ttu-id="49775-102">AddNew (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="49775-102">AddNew method (ADO)</span></span>


<span data-ttu-id="49775-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49775-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49775-104">Crea un nuevo registro de un objeto [Recordset](recordset-object-ado.md) actualizable.</span><span class="sxs-lookup"><span data-stu-id="49775-104">Creates a new record for an updatable [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="49775-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49775-105">Syntax</span></span>

<span data-ttu-id="49775-106">*conjunto de registros*. AddNew *listaDeCampos*, *valores*</span><span class="sxs-lookup"><span data-stu-id="49775-106">*recordset*.AddNew *FieldList*, *Values*</span></span>

## <a name="parameters"></a><span data-ttu-id="49775-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49775-107">Parameters</span></span>

  - <span data-ttu-id="49775-108">*recordset*</span><span class="sxs-lookup"><span data-stu-id="49775-108">*recordset*</span></span>

  - <span data-ttu-id="49775-109">Un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="49775-109">A **Recordset** object.</span></span>

  - <span data-ttu-id="49775-110">*Lista de campos*</span><span class="sxs-lookup"><span data-stu-id="49775-110">*FieldList*</span></span>

  - <span data-ttu-id="49775-p101">Es opcional. Un solo nombre o una matriz de nombres o posiciones ordinales de los campos en el nuevo registro.</span><span class="sxs-lookup"><span data-stu-id="49775-p101">Optional. A single name, or an array of names or ordinal positions of the fields in the new record.</span></span>

  - <span data-ttu-id="49775-113">*Values*</span><span class="sxs-lookup"><span data-stu-id="49775-113">*Values*</span></span>

  - <span data-ttu-id="49775-114">Es opcional.</span><span class="sxs-lookup"><span data-stu-id="49775-114">Optional.</span></span> <span data-ttu-id="49775-115">Un solo valor o una matriz de valores para los campos en el registro nuevo.</span><span class="sxs-lookup"><span data-stu-id="49775-115">A single value, or an array of values for the fields in the new record.</span></span> <span data-ttu-id="49775-116">Si *Fieldlist* es una matriz, *los valores* también debe ser una matriz con el mismo número de miembros; de lo contrario, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="49775-116">If *Fieldlist* is an array, *Values* must also be an array with the same number of members; otherwise, an error occurs.</span></span> <span data-ttu-id="49775-117">El orden de los nombres de campo debe coincidir con el orden de los valores de campo en cada matriz.</span><span class="sxs-lookup"><span data-stu-id="49775-117">The order of field names must match the order of field values in each array.</span></span>

## <a name="remarks"></a><span data-ttu-id="49775-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="49775-118">Remarks</span></span>

<span data-ttu-id="49775-p103">Use el método **AddNew** para crear e inicializar un registro nuevo. Utilice el método [Supports](supports-method-ado.md) con **adAddNew** (un valor de [CursorOptionEnum](cursoroptionenum.md)) para comprobar si puede agregar registros al actual objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="49775-p103">Use the **AddNew** method to create and initialize a new record. Use the [Supports](supports-method-ado.md) method with **adAddNew** (a [CursorOptionEnum](cursoroptionenum.md) value) to verify whether you can add records to the current **Recordset** object.</span></span>

<span data-ttu-id="49775-p104">Tras llamar al método **AddNew**, el registro nuevo se convierte en el registro actual y permanece actual después de llamar al método [Update](update-method-ado.md). Dado que el registro nuevo se anexa al objeto **Recordset**, una llamada a **MoveNext** después de la llamada a Update hará que se realice un desplazamiento hasta más allá del final del objeto **Recordset**, por lo que el valor de **EOF** será True. Si el objeto **Recordset** no admite marcadores, es posible que no pueda obtener acceso al nuevo registro cuando se mueva a otro registro. Dependiendo del tipo de cursor, puede que tenga que llamar al método [Requery](requery-method-ado.md) para que el registro nuevo sea accesible.</span><span class="sxs-lookup"><span data-stu-id="49775-p104">After you call the **AddNew** method, the new record becomes the current record and remains current after you call the [Update](update-method-ado.md) method. Since the new record is appended to the **Recordset**, a call to **MoveNext** following the Update will move past the end of the **Recordset**, making **EOF** True. If the **Recordset** object does not support bookmarks, you may not be able to access the new record once you move to another record. Depending on your cursor type, you may need to call the [Requery](requery-method-ado.md) method to make the new record accessible.</span></span>

<span data-ttu-id="49775-125">Si llama a **AddNew** mientras modifica el registro actual o agrega un registro nuevo, ADO llamará al método **Update** para guardar todos los cambios y, después, ADO creará el registro nuevo.</span><span class="sxs-lookup"><span data-stu-id="49775-125">If you call **AddNew** while editing the current record or while adding a new record, ADO calls the **Update** method to save any changes and then creates the new record.</span></span>

<span data-ttu-id="49775-126">El comportamiento del método **AddNew** depende del modo de actualización del objeto **Recordset** y si se pasan los argumentos *Fieldlist* y *Values* .</span><span class="sxs-lookup"><span data-stu-id="49775-126">The behavior of the **AddNew** method depends on the updating mode of the **Recordset** object and whether you pass the *Fieldlist* and *Values* arguments.</span></span>

<span data-ttu-id="49775-p105">En el *modo de actualización inmediata* (donde el proveedor escribe los cambios en el origen de datos subyacente cuando se llama al método **Update**), si llama al método **AddNew** sin argumentos, la propiedad [EditMode](editmode-property-ado.md) se establece en **adEditAdd** (un valor de [EditModeEnum](editmodeenum.md)). El proveedor almacena en la memoria caché local todos los cambios de los valores de campo. Si llama al método **Update**, se envía el nuevo registro a la base de datos y se restablece la propiedad **EditMode** en **adEditNone** (un valor de **EditModeEnum**). Si pasa los argumentos *Fieldlist* y *Values*, ADO envía inmediatamente el nuevo registro a la base de datos (no es necesario llamar a **Update**); el valor de la propiedad **EditMode** no cambia (**adEditNone**).</span><span class="sxs-lookup"><span data-stu-id="49775-p105">In *immediate update mode* (in which the provider writes changes to the underlying data source once you call the **Update** method), calling the **AddNew** method without arguments sets the [EditMode](editmode-property-ado.md) property to **adEditAdd** (an [EditModeEnum](editmodeenum.md) value). The provider caches any field value changes locally. Calling the **Update** method posts the new record to the database and resets the **EditMode** property to **adEditNone** (an **EditModeEnum** value). If you pass the *Fieldlist* and *Values* arguments, ADO immediately posts the new record to the database (no **Update** call is necessary); the **EditMode** property value does not change (**adEditNone**).</span></span>

<span data-ttu-id="49775-131">En *el modo de actualización por lotes* (en el que el proveedor almacena varios cambios en caché y los escribe en el origen de datos subyacente sólo cuando se llama al método [UpdateBatch](updatebatch-method-ado.md) ), si se llama al método **AddNew** sin argumentos establece el **EditMode** propiedad **adEditAdd**.</span><span class="sxs-lookup"><span data-stu-id="49775-131">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd**.</span></span> <span data-ttu-id="49775-132">El proveedor almacena en caché localmente los cambios de valor de campo.</span><span class="sxs-lookup"><span data-stu-id="49775-132">The provider caches any field value changes locally.</span></span> <span data-ttu-id="49775-133">Si se llama al método **Update**, el nuevo registro se agrega al **conjunto de registros** activo y la propiedad **EditMode** se restablece en **adEditNone**, pero el proveedor no envía los cambios a la base de datos subyacente hasta que se llame al método **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="49775-133">Calling the **Update** method adds the new record to the current **Recordset** and resets the **EditMode** property to **adEditNone**, but the provider does not post the changes to the underlying database until you call the **UpdateBatch** method.</span></span> <span data-ttu-id="49775-134">Si se pasan los argumentos *Fieldlist* y *Values* , ADO envía el nuevo registro al proveedor para el almacenamiento en caché; debe llamar al método **UpdateBatch** para enviar el nuevo registro a la base de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="49775-134">If you pass the *Fieldlist* and *Values* arguments, ADO sends the new record to the provider for storage in a cache; you need to call the **UpdateBatch** method to post the new record to the underlying database.</span></span>

