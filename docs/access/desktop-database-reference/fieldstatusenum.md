---
title: FieldStatusEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: FieldStatusEnum
ms:assetid: 49570042-8435-8618-3ba1-7006c47735e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249225(v=office.15)
ms:contentKeyID: 48544635
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 22c5d53427d1380273ea82b3a28ae044e103b179
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860612"
---
# <a name="fieldstatusenum"></a><span data-ttu-id="d6d73-102">FieldStatusEnum</span><span class="sxs-lookup"><span data-stu-id="d6d73-102">FieldStatusEnum</span></span>

<span data-ttu-id="d6d73-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6d73-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d6d73-104">Especifica el estado de un objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="d6d73-104">Specifies the status of a **Field** object.</span></span>

<span data-ttu-id="d6d73-105">Los valores **adFieldPending\*** indican la operación que provocó el estado, y se pueden combinar con otros valores de estado.</span><span class="sxs-lookup"><span data-stu-id="d6d73-105">The **adFieldPending\*** values indicate the operation that caused the status to be set, and may be combined with other status values.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6d73-106">Constante</span><span class="sxs-lookup"><span data-stu-id="d6d73-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="d6d73-107">Valor</span><span class="sxs-lookup"><span data-stu-id="d6d73-107">Value</span></span></p></th>
<th><p><span data-ttu-id="d6d73-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6d73-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6d73-109"><strong>adFieldAlreadyExists</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-109"><strong>adFieldAlreadyExists</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-110">26</span><span class="sxs-lookup"><span data-stu-id="d6d73-110">26</span></span></p></td>
<td><p><span data-ttu-id="d6d73-111">Indica que ya existe el campo especificado.</span><span class="sxs-lookup"><span data-stu-id="d6d73-111">Indicates that the specified field already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6d73-112"><strong>adFieldBadStatus</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-112"><strong>adFieldBadStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-113">12</span><span class="sxs-lookup"><span data-stu-id="d6d73-113">12</span></span></p></td>
<td><p><span data-ttu-id="d6d73-p101">Indica que se envió al proveedor OLE DB un valor de estado no válido desde ADO. Entre otras causas posibles, se incluyen un proveedor OLE DB 1.0 o 1.1 o una combinación incorrecta de <a href="value-property-ado.md">Value</a> y de <a href="status-property-ado-field.md">Status</a>.</span><span class="sxs-lookup"><span data-stu-id="d6d73-p101">Indicates that an invalid status value was sent from ADO to the OLE DB provider. Possible causes include an OLE DB 1.0 or 1.1 provider, or an improper combination of <a href="value-property-ado.md">Value</a> and <a href="status-property-ado-field.md">Status</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6d73-116"><strong>adFieldCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-116"><strong>adFieldCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-117">20</span><span class="sxs-lookup"><span data-stu-id="d6d73-117">20</span></span></p></td>
<td><p><span data-ttu-id="d6d73-118">Indica que el servidor de la dirección URL especificada por <a href="source-property-ado-record.md">Source</a> no pudo completar la operación.</span><span class="sxs-lookup"><span data-stu-id="d6d73-118">Indicates that the server of the URL specified by <a href="source-property-ado-record.md">Source</a> could not complete the operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6d73-119"><strong>adFieldCannotDeleteSource</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-119"><strong>adFieldCannotDeleteSource</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-120">23</span><span class="sxs-lookup"><span data-stu-id="d6d73-120">23</span></span></p></td>
<td><p><span data-ttu-id="d6d73-121">Indica una operación en la que un árbol o un subárbol se movió a una ubicación nueva pero no se pudo eliminar el origen.</span><span class="sxs-lookup"><span data-stu-id="d6d73-121">Indicates that during a move operation, a tree or subtree was moved to a new location, but the source could not be deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6d73-122"><strong>adFieldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-122"><strong>adFieldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-123">2</span><span class="sxs-lookup"><span data-stu-id="d6d73-123">2</span></span></p></td>
<td><p><span data-ttu-id="d6d73-124">Indica que el campo no se puede recuperar ni almacenar sin pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="d6d73-124">Indicates that the field cannot be retrieved or stored without loss of data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6d73-125"><strong>adFieldCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-125"><strong>adFieldCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-126">7</span><span class="sxs-lookup"><span data-stu-id="d6d73-126">7</span></span></p></td>
<td><p><span data-ttu-id="d6d73-127">Indica que no se pudo agregar el campo a causa de que el proveedor superó una limitación (como el número de campos admitidos).</span><span class="sxs-lookup"><span data-stu-id="d6d73-127">Indicates that the field could not be added because the provider exceeded a limitation (such as the number of fields allowed).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6d73-128"><strong>adFieldDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-128"><strong>adFieldDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-129">6</span><span class="sxs-lookup"><span data-stu-id="d6d73-129">6</span></span></p></td>
<td><p><span data-ttu-id="d6d73-130">Indica que los datos devueltos desde el proveedor desbordaron el tipo de datos del campo.</span><span class="sxs-lookup"><span data-stu-id="d6d73-130">Indicates that the data returned from the provider overflowed the data type of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6d73-131"><strong>adFieldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-131"><strong>adFieldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-132">13</span><span class="sxs-lookup"><span data-stu-id="d6d73-132">13</span></span></p></td>
<td><p><span data-ttu-id="d6d73-133">Indica que se utilizó el valor predeterminado del campo al configurar datos.</span><span class="sxs-lookup"><span data-stu-id="d6d73-133">Indicates that the default value for the field was used when setting data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6d73-134"><strong>adFieldDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-134"><strong>adFieldDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-135">16</span><span class="sxs-lookup"><span data-stu-id="d6d73-135">16</span></span></p></td>
<td><p><span data-ttu-id="d6d73-136">Indica que no existe el campo especificado.</span><span class="sxs-lookup"><span data-stu-id="d6d73-136">Indicates that the field specified does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6d73-137"><strong>adFieldIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-137"><strong>adFieldIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-138">15</span><span class="sxs-lookup"><span data-stu-id="d6d73-138">15</span></span></p></td>
<td><p><span data-ttu-id="d6d73-p102">Indica que se omitió este campo al establecer los valores de los datos en el origen. El proveedor no estableció ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d6d73-p102">Indicates that this field was skipped when setting data values in the source. The provider set no value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6d73-141"><strong>adFieldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-141"><strong>adFieldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-142">10</span><span class="sxs-lookup"><span data-stu-id="d6d73-142">10</span></span></p></td>
<td><p><span data-ttu-id="d6d73-143">Indica que el campo no se puede modificar porque es una entidad calculada o derivada.</span><span class="sxs-lookup"><span data-stu-id="d6d73-143">Indicates that the field cannot be modified because it is a calculated or derived entity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6d73-144"><strong>adFieldInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-144"><strong>adFieldInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-145">17</span><span class="sxs-lookup"><span data-stu-id="d6d73-145">17</span></span></p></td>
<td><p><span data-ttu-id="d6d73-146">Indica que la dirección URL del origen de datos contiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="d6d73-146">Indicates that the data source URL contains invalid characters.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6d73-147"><strong>adFieldIsNull</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-147"><strong>adFieldIsNull</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-148">3</span><span class="sxs-lookup"><span data-stu-id="d6d73-148">3</span></span></p></td>
<td><p><span data-ttu-id="d6d73-149">Indica que el proveedor devolvió un valor VARIANT de tipo VT_NULL y que el campo no está vacío.</span><span class="sxs-lookup"><span data-stu-id="d6d73-149">Indicates that the provider returned a VARIANT value of type VT_NULL and that the field is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6d73-150"><strong>adFieldOK</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-150"><strong>adFieldOK</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-151">0</span><span class="sxs-lookup"><span data-stu-id="d6d73-151">0</span></span></p></td>
<td><p><span data-ttu-id="d6d73-p103">Valor predeterminado. Indica que el campo se agregó o se eliminó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d6d73-p103">Default. Indicates that the field was successfully added or deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6d73-154"><strong>adFieldOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-154"><strong>adFieldOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-155">22</span><span class="sxs-lookup"><span data-stu-id="d6d73-155">22</span></span></p></td>
<td><p><span data-ttu-id="d6d73-156">Indica que el proveedor no puede obtener suficiente espacio de almacenamiento para completar una operación de movimiento o de copia.</span><span class="sxs-lookup"><span data-stu-id="d6d73-156">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6d73-157"><strong>adFieldPendingChange</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-157"><strong>adFieldPendingChange</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-158">0 x 40000</span><span class="sxs-lookup"><span data-stu-id="d6d73-158">0x40000</span></span></p></td>
<td><p><span data-ttu-id="d6d73-p104">Indica que el valor del campo ha sido eliminado y luego agregado de nuevo, quizá con un tipo de datos diferente, o que el valor del campo que antes tenía un estado adFieldOK ha cambiado. La forma final del campo modificará la colección <a href="fields-collection-ado.md">Fields</a> después de llamar al método <a href="update-method-ado.md">Update</a>.</span><span class="sxs-lookup"><span data-stu-id="d6d73-p104">Indicates either that the field has been deleted and then re-added, perhaps with a different data type, or that the value of the field that previously had a status of adFieldOK has changed. The final form of the field will modify the <a href="fields-collection-ado.md">Fields</a> collection after the <a href="update-method-ado.md">Update</a> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6d73-161"><strong>adFieldPendingDelete</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-161"><strong>adFieldPendingDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-162">0 x 20000</span><span class="sxs-lookup"><span data-stu-id="d6d73-162">0x20000</span></span></p></td>
<td><p><span data-ttu-id="d6d73-p105">Indica que la operación <strong>Delete</strong> provocó el establecimiento del estado. El campo ha sido marcado para su eliminación de la colección <strong>Fields</strong> después de la llamada al método <strong>Update</strong>.</span><span class="sxs-lookup"><span data-stu-id="d6d73-p105">Indicates that the <strong>Delete</strong> operation caused the status to be set. The field has been marked for deletion from the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6d73-165"><strong>adFieldPendingInsert</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-165"><strong>adFieldPendingInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-166">0 x 10000</span><span class="sxs-lookup"><span data-stu-id="d6d73-166">0x10000</span></span></p></td>
<td><p><span data-ttu-id="d6d73-p106">Indica que la operación <strong>Append</strong> provocó el establecimiento del estado. El objeto <strong>Field</strong> (campo) ha sido marcado para su eliminación de la colección <strong>Fields</strong> después de la llamada al método <strong>Update</strong>.</span><span class="sxs-lookup"><span data-stu-id="d6d73-p106">Indicates that the <strong>Append</strong> operation caused the status to be set. The <strong>Field</strong> has been marked to be added to the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6d73-169"><strong>adFieldPendingUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-169"><strong>adFieldPendingUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-170">0 x 80000</span><span class="sxs-lookup"><span data-stu-id="d6d73-170">0x80000</span></span></p></td>
<td><p><span data-ttu-id="d6d73-171">Indica que el proveedor no puede determinar qué operación causó el establecimiento del estado del campo.</span><span class="sxs-lookup"><span data-stu-id="d6d73-171">Indicates that the provider cannot determine what operation caused field status to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6d73-172"><strong>adFieldPendingUnknownDelete</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-172"><strong>adFieldPendingUnknownDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-173">0 x 100000</span><span class="sxs-lookup"><span data-stu-id="d6d73-173">0x100000</span></span></p></td>
<td><p><span data-ttu-id="d6d73-174">Indica que el proveedor no puede determinar qué operación causó el establecimiento del estado del campo, y que el campo se eliminará de la colección <strong>Fields</strong> después de la llamada al método <strong>Update</strong>.</span><span class="sxs-lookup"><span data-stu-id="d6d73-174">Indicates that the provider cannot determine what operation caused field status to be set, and that the field will be deleted from the <strong>Fields</strong> collection after the <strong>Update</strong> method is called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6d73-175"><strong>adFieldPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-175"><strong>adFieldPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-176">9</span><span class="sxs-lookup"><span data-stu-id="d6d73-176">9</span></span></p></td>
<td><p><span data-ttu-id="d6d73-177">Indica que no se puede modificar el campo debido a que se ha definido como de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="d6d73-177">Indicates that the field cannot be modified because it is defined as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6d73-178"><strong>adFieldReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-178"><strong>adFieldReadOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-179">24</span><span class="sxs-lookup"><span data-stu-id="d6d73-179">24</span></span></p></td>
<td><p><span data-ttu-id="d6d73-180">Indica que el campo del origen de datos se ha definido como de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="d6d73-180">Indicates that the field in the data source is defined as read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6d73-181"><strong>adFieldResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-181"><strong>adFieldResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-182">19</span><span class="sxs-lookup"><span data-stu-id="d6d73-182">19</span></span></p></td>
<td><p><span data-ttu-id="d6d73-183">Indica que el proveedor no pudo realizar la operación porque ya existe un objeto en la dirección URL de destino y no es posible sobrescribir el objeto.</span><span class="sxs-lookup"><span data-stu-id="d6d73-183">Indicates that the provider was unable to perform the operation because an object already exists at the destination URL and it is not able to overwrite the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6d73-184"><strong>adFieldResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-184"><strong>adFieldResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-185">18</span><span class="sxs-lookup"><span data-stu-id="d6d73-185">18</span></span></p></td>
<td><p><span data-ttu-id="d6d73-186">Indica que el proveedor no pudo realizar la operación a causa de que el origen de datos está bloqueado por otros procesos o aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d6d73-186">Indicates that the provider was unable to perform the operation because the data source is locked by one or more other application or process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6d73-187"><strong>adFieldResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-187"><strong>adFieldResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-188">25</span><span class="sxs-lookup"><span data-stu-id="d6d73-188">25</span></span></p></td>
<td><p><span data-ttu-id="d6d73-189">Indica que una dirección URL de origen o destino está fuera del ámbito del registro actual.</span><span class="sxs-lookup"><span data-stu-id="d6d73-189">Indicates that a source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6d73-190"><strong>adFieldSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-190"><strong>adFieldSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-191">11</span><span class="sxs-lookup"><span data-stu-id="d6d73-191">11</span></span></p></td>
<td><p><span data-ttu-id="d6d73-192">Indica que el valor no cumplió la restricción del esquema del origen de datos para el campo.</span><span class="sxs-lookup"><span data-stu-id="d6d73-192">Indicates that the value violated the data source schema constraint for the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6d73-193"><strong>adFieldSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-193"><strong>adFieldSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-194">5</span><span class="sxs-lookup"><span data-stu-id="d6d73-194">5</span></span></p></td>
<td><p><span data-ttu-id="d6d73-195">Indica que el valor de datos devuelto por el proveedor tenía signo, pero el tipo de datos del valor del campo ADO no.</span><span class="sxs-lookup"><span data-stu-id="d6d73-195">Indicates that data value returned by the provider was signed but the data type of the ADO field value was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6d73-196"><strong>adFieldTruncated</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-196"><strong>adFieldTruncated</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-197">4</span><span class="sxs-lookup"><span data-stu-id="d6d73-197">4</span></span></p></td>
<td><p><span data-ttu-id="d6d73-198">Indica que se truncaron datos de longitud variable al leer el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="d6d73-198">Indicates that variable-length data was truncated when reading from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6d73-199"><strong>adFieldUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-199"><strong>adFieldUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-200">8</span><span class="sxs-lookup"><span data-stu-id="d6d73-200">8</span></span></p></td>
<td><p><span data-ttu-id="d6d73-p107">Indica que el proveedor no pudo determinar el valor al leer el origen de datos. Por ejemplo, la fila estaba recién creada, el valor predeterminado de la columna no estaba disponible y no se había aún especificado un nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="d6d73-p107">Indicates that the provider could not determine the value when reading from the data source. For example, the row was just created, the default value for the column was not available, and a new value had not yet been specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6d73-203"><strong>adFieldVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="d6d73-203"><strong>adFieldVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="d6d73-204">21</span><span class="sxs-lookup"><span data-stu-id="d6d73-204">21</span></span></p></td>
<td><p><span data-ttu-id="d6d73-205">Indica que el proveedor no puede encontrar el volumen de almacenamiento indicado por la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="d6d73-205">Indicates that the provider is unable to locate the storage volume indicated by the URL.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="d6d73-206">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="d6d73-206">ADO/WFC equivalent</span></span>

<span data-ttu-id="d6d73-207">Estas constantes no tienen equivalentes ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="d6d73-207">These constants do not have ADO/WFC equivalents.</span></span>

