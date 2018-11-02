---
title: Propiedad Recordset.RecordsetType (DAO)
TOCTitle: RecordsetType Property
ms:assetid: a66d4043-08cc-ead1-f9ff-efc7d7ea21bf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821178(v=office.15)
ms:contentKeyID: 48546853
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13361
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e521c4de48f45d080a3b201ac431b2d7da14bc22
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923227"
---
# <a name="recordsetrecordsettype-property-dao"></a><span data-ttu-id="c0b11-102">Propiedad Recordset.RecordsetType (DAO)</span><span class="sxs-lookup"><span data-stu-id="c0b11-102">Recordset.RecordsetType property (DAO)</span></span>

<span data-ttu-id="c0b11-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0b11-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c0b11-p101">Puede utilizar la propiedad **RecordsetType** para especificar el tipo de conjunto de registros que se hace disponible para un formulario. **Byte** de Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c0b11-p101">You can use the **RecordsetType** property to specify what kind of recordset is made available to a form. Read/write **Byte**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0b11-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0b11-106">Syntax</span></span>

<span data-ttu-id="c0b11-107">*expresión* . RecordsetType</span><span class="sxs-lookup"><span data-stu-id="c0b11-107">*expression* .RecordsetType</span></span>

<span data-ttu-id="c0b11-108">*expression* Variable que representa un objeto **Form**.</span><span class="sxs-lookup"><span data-stu-id="c0b11-108">*expression* A variable that represents a **Form** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0b11-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c0b11-109">Remarks</span></span>

<span data-ttu-id="c0b11-110">La propiedad **RecordsetType** usa los siguientes valores en una base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c0b11-110">The **RecordsetType** property uses the following settings in a Microsoft Access database.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c0b11-111">Valor</span><span class="sxs-lookup"><span data-stu-id="c0b11-111">Setting</span></span></p></th>
<th><p><span data-ttu-id="c0b11-112">Tipo de conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="c0b11-112">Type of Recordset</span></span></p></th>
<th><p><span data-ttu-id="c0b11-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0b11-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0b11-114">0</span><span class="sxs-lookup"><span data-stu-id="c0b11-114">0</span></span></p></td>
<td><p><span data-ttu-id="c0b11-115">Dynaset</span><span class="sxs-lookup"><span data-stu-id="c0b11-115">Dynaset</span></span></p></td>
<td><p><span data-ttu-id="c0b11-116">(Valor predeterminado) Puede modificar controles dependientes basados en una sola tabla o tablas con una relación uno a uno.</span><span class="sxs-lookup"><span data-stu-id="c0b11-116">(Default) You can edit bound controls based on a single table or tables with a one-to-one relationship.</span></span> <span data-ttu-id="c0b11-117">Para controles dependientes de campos basados en tablas con una relación uno a varios, no se puede editar los datos del campo de combinación en la &quot;una&quot; lateral de la relación, a menos que está habilitada la actualización en cascada entre las tablas.</span><span class="sxs-lookup"><span data-stu-id="c0b11-117">For controls bound to fields based on tables with a one-to-many relationship, you can't edit data from the join field on the &quot;one&quot; side of the relationship unless cascade update is enabled between the tables.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0b11-118">1</span><span class="sxs-lookup"><span data-stu-id="c0b11-118">1</span></span></p></td>
<td><p><span data-ttu-id="c0b11-119">Dynaset (Actualizaciones no coherentes)</span><span class="sxs-lookup"><span data-stu-id="c0b11-119">Dynaset (Inconsistent Updates)</span></span></p></td>
<td><p><span data-ttu-id="c0b11-120">Se pueden editar todas las tablas y los controles vinculados a sus campos.</span><span class="sxs-lookup"><span data-stu-id="c0b11-120">All tables and controls bound to their fields can be edited.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0b11-121">2</span><span class="sxs-lookup"><span data-stu-id="c0b11-121">2</span></span></p></td>
<td><p><span data-ttu-id="c0b11-122">Snapshot</span><span class="sxs-lookup"><span data-stu-id="c0b11-122">Snapshot</span></span></p></td>
<td><p><span data-ttu-id="c0b11-123">No se puede editar las tablas o sus controles dependientes.</span><span class="sxs-lookup"><span data-stu-id="c0b11-123">No tables or the controls bound to their fields can be edited.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="c0b11-124">[!NOTA] Si no desea que se puedan modificar los datos de controles dependientes cuando un formulario está en la vista Formulario o en la vista Hoja de datos, puede establecer la propiedad **RecordsetType** en 2.</span><span class="sxs-lookup"><span data-stu-id="c0b11-124">If you don't want data in bound controls to be edited when a form is in Form view or Datasheet view, you can set the **RecordsetType** property to 2.</span></span>



<span data-ttu-id="c0b11-125">La propiedad **RecordsetType** usa los siguientes valores en un proyecto de Microsoft Access (.ADP).</span><span class="sxs-lookup"><span data-stu-id="c0b11-125">The **RecordsetType** property uses the following settings in a Microsoft Access project (.adp).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c0b11-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c0b11-126">Setting</span></span></p></th>
<th><p><span data-ttu-id="c0b11-127">Tipo de conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="c0b11-127">Type of Recordset</span></span></p></th>
<th><p><span data-ttu-id="c0b11-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0b11-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0b11-129">3</span><span class="sxs-lookup"><span data-stu-id="c0b11-129">3</span></span></p></td>
<td><p><span data-ttu-id="c0b11-130">Snapshot</span><span class="sxs-lookup"><span data-stu-id="c0b11-130">Snapshot</span></span></p></td>
<td><p><span data-ttu-id="c0b11-131">No se puede editar las tablas o sus controles dependientes.</span><span class="sxs-lookup"><span data-stu-id="c0b11-131">No tables or the controls bound to their fields can be edited.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0b11-132">4</span><span class="sxs-lookup"><span data-stu-id="c0b11-132">4</span></span></p></td>
<td><p><span data-ttu-id="c0b11-133">Snapshot actualizable</span><span class="sxs-lookup"><span data-stu-id="c0b11-133">Updatable Snapshot</span></span></p></td>
<td><p><span data-ttu-id="c0b11-134">(Valor predeterminado) Se pueden modificar todas las tablas y los controles dependientes de sus campos.</span><span class="sxs-lookup"><span data-stu-id="c0b11-134">(Default) All tables and controls bound to their fields can be edited.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="c0b11-135">[!NOTA] Si se modifica la propiedad **RecordsetType** de un formulario o informe abierto, se vuelve a crear automáticamente el conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="c0b11-135">Changing the **RecordsetType** property of an open form or report causes an automatic recreation of the recordset.</span></span>



<span data-ttu-id="c0b11-p103">Puede crear formularios basados en varias tablas base con campos vinculados a los controles del formulario. Según el valor de la propiedad **RecordsetType**, podrá limitar qué control dependiente se puede editar.</span><span class="sxs-lookup"><span data-stu-id="c0b11-p103">You can create forms based on multiple underlying tables with fields bound to controls on the forms. Depending on the **RecordsetType** property setting, you can limit which of these bound controls can be edited.</span></span>

<span data-ttu-id="c0b11-138">Además de la edición del control proporcionada por la **propiedad RecordsetType**, cada control de un formulario tiene una propiedad **Locked** que puede establecer para especificar si se pueden editar el control y sus datos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="c0b11-138">In addition to the editing control provided by **RecordsetType**, each control on a form has a **Locked** property that you can set to specify whether the control and its underlying data can be edited.</span></span> <span data-ttu-id="c0b11-139">Si la propiedad **Locked** se establece en Yes, no se podrán editar los datos.</span><span class="sxs-lookup"><span data-stu-id="c0b11-139">If the **Locked** property is set to Yes, you can't edit the data.</span></span>

## <a name="example"></a><span data-ttu-id="c0b11-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c0b11-140">Example</span></span>

<span data-ttu-id="c0b11-p105">En el siguiente ejemplo, se podrán editar los datos solo cuando la identificación del usuario sea Admin. Este ejemplo de código establece la propiedad **RecordsetType** a Snapshot si la variable pública  no es ADMIN.</span><span class="sxs-lookup"><span data-stu-id="c0b11-p105">In the following example, only if the user ID is ADMIN can records be updated. This code sample sets the **RecordsetType** property to Snapshot if the public variable gstrUserID value is not ADMIN.</span></span>

```vb
    Sub Form_Open(Cancel As Integer) 
     Const conSnapshot = 2 
     If gstrUserID <> "ADMIN" Then 
     Forms!Employees.RecordsetType = conSnapshot 
     End If 
    End Sub
```

## <a name="see-also"></a><span data-ttu-id="c0b11-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c0b11-143">See also</span></span>

- [<span data-ttu-id="c0b11-144">Objeto Form</span><span class="sxs-lookup"><span data-stu-id="c0b11-144">Form Object</span></span>](https://docs.microsoft.com/office/vba/api/Access.Form)


