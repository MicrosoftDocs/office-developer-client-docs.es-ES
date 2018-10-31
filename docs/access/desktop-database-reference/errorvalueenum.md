---
title: ErrorValueEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: ErrorValueEnum
ms:assetid: 2af99f32-6004-1225-367c-45d693f447b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249058(v=office.15)
ms:contentKeyID: 48543921
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 5e9da9b9c197bb9917d2184e07a76bdfb25bd031
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860867"
---
# <a name="errorvalueenum"></a><span data-ttu-id="066ff-102">ErrorValueEnum</span><span class="sxs-lookup"><span data-stu-id="066ff-102">ErrorValueEnum</span></span>

<span data-ttu-id="066ff-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="066ff-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="066ff-104">Especifica el tipo de error ADO en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="066ff-104">Specifies the type of ADO run-time error.</span></span>

<span data-ttu-id="066ff-105">Se muestran tres formas del número de error:</span><span class="sxs-lookup"><span data-stu-id="066ff-105">Three forms of the error number are listed:</span></span>

- <span data-ttu-id="066ff-p101">Decimal positivo: los dos bytes bajos del número completo en formato decimal. Este número aparece en el cuadro de diálogo predeterminado de mensaje de error de Visual Basic. Por ejemplo, Error en tiempo de ejecución "3707".</span><span class="sxs-lookup"><span data-stu-id="066ff-p101">Positive decimal — the low two bytes of the full number in decimal format. This number is displayed in the default Visual Basic error message dialog box. For example, Run-time error '3707'.</span></span>

- <span data-ttu-id="066ff-109">Decimal negativo: la traducción decimal del número de error completo.</span><span class="sxs-lookup"><span data-stu-id="066ff-109">Negative decimal — The decimal translation of the full error number.</span></span>

- <span data-ttu-id="066ff-p102">Hexadecimal: la representación hexadecimal del número de error completo. El código de servicio de Windows se encuentra en el cuarto dígito. El código de servicio para números de error ADO es *A*. Por ejemplo: 0x800***A***0E7B.</span><span class="sxs-lookup"><span data-stu-id="066ff-p102">Hexadecimal — The hexadecimal representation of the full error number. The Windows facility code is in the fourth digit. The facility code for ADO error numbers is *A*. For example: 0x800***A***0E7B.</span></span>

> [!NOTE]
> <span data-ttu-id="066ff-113">Errores de OLE DB se pueden pasar a una aplicación de ADO.</span><span class="sxs-lookup"><span data-stu-id="066ff-113">OLE DB errors may be passed to your ADO application.</span></span> <span data-ttu-id="066ff-114">Normalmente, estos se pueden identificar por un código de servicio de Windows de *4*.</span><span class="sxs-lookup"><span data-stu-id="066ff-114">Typically, these can be identified by a Windows facility code of *4*.</span></span> <span data-ttu-id="066ff-115">Por ejemplo, 0x800_**4**_... Para obtener más información acerca de estos números, consulte el capítulo 16 de la *referencia del programador de OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="066ff-115">For example, 0x800_**4**_.... For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="066ff-116">Constante</span><span class="sxs-lookup"><span data-stu-id="066ff-116">Constant</span></span></p></th>
<th><p><span data-ttu-id="066ff-117">Valor</span><span class="sxs-lookup"><span data-stu-id="066ff-117">Value</span></span></p></th>
<th><p><span data-ttu-id="066ff-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="066ff-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="066ff-119"><strong>adErrBoundToCommand</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-119"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-120">3707</span><span class="sxs-lookup"><span data-stu-id="066ff-120">3707</span></span><br />
<span data-ttu-id="066ff-121">-2146824581</span><span class="sxs-lookup"><span data-stu-id="066ff-121">-2146824581</span></span><br />
<span data-ttu-id="066ff-122">0x800A0E7B</span><span class="sxs-lookup"><span data-stu-id="066ff-122">0x800A0E7B</span></span></p></td>
<td><p><span data-ttu-id="066ff-123">No se puede cambiar la propiedad <strong>ActiveConnection</strong> de un objeto <strong>Recordset</strong> que tiene un objeto <strong>Command</strong> como su origen.</span><span class="sxs-lookup"><span data-stu-id="066ff-123">Cannot change the <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object which has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-124"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-124"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-125">3732</span><span class="sxs-lookup"><span data-stu-id="066ff-125">3732</span></span><br />
<span data-ttu-id="066ff-126">-2146824556</span><span class="sxs-lookup"><span data-stu-id="066ff-126">-2146824556</span></span><br />
<span data-ttu-id="066ff-127">0x800A0E94</span><span class="sxs-lookup"><span data-stu-id="066ff-127">0x800A0E94</span></span></p></td>
<td><p><span data-ttu-id="066ff-128">El servidor no puede completar la operación.</span><span class="sxs-lookup"><span data-stu-id="066ff-128">Server cannot complete the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-129"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-129"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-130">3748</span><span class="sxs-lookup"><span data-stu-id="066ff-130">3748</span></span><br />
<span data-ttu-id="066ff-131">-2146824540</span><span class="sxs-lookup"><span data-stu-id="066ff-131">-2146824540</span></span><br />
<span data-ttu-id="066ff-132">0x800A0EA4</span><span class="sxs-lookup"><span data-stu-id="066ff-132">0x800A0EA4</span></span></p></td>
<td><p><span data-ttu-id="066ff-p104">Se denegó conexión. La conexión nueva que solicitó tiene características diferentes de la que ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="066ff-p104">Connection was denied. New connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-135"><strong>adErrCantChangeProvider</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-135"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-136">3220</span><span class="sxs-lookup"><span data-stu-id="066ff-136">3220</span></span><br />
<span data-ttu-id="066ff-137">-2146825068</span><span class="sxs-lookup"><span data-stu-id="066ff-137">-2146825068</span></span><br />
<span data-ttu-id="066ff-138">0X800A0C94</span><span class="sxs-lookup"><span data-stu-id="066ff-138">0X800A0C94</span></span></p></td>
<td><p><span data-ttu-id="066ff-139">El proveedor suministrado es distinto del que se está utilizando.</span><span class="sxs-lookup"><span data-stu-id="066ff-139">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-140"><strong>adErrCantConvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-140"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-141">3724</span><span class="sxs-lookup"><span data-stu-id="066ff-141">3724</span></span><br />
<span data-ttu-id="066ff-142">-2146824564</span><span class="sxs-lookup"><span data-stu-id="066ff-142">-2146824564</span></span><br />
<span data-ttu-id="066ff-143">0x800A0E8C</span><span class="sxs-lookup"><span data-stu-id="066ff-143">0x800A0E8C</span></span></p></td>
<td><p><span data-ttu-id="066ff-p105">El valor de los datos no se puede convertir por motivos distintos a un desajuste entre signos o a un desbordamiento de datos. Por ejemplo, puede que la conversión haya truncado datos.</span><span class="sxs-lookup"><span data-stu-id="066ff-p105">Data value cannot be converted for reasons other than sign mismatch or data overflow. For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-146"><strong>adErrCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-146"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-147">3725</span><span class="sxs-lookup"><span data-stu-id="066ff-147">3725</span></span><br />
<span data-ttu-id="066ff-148">-2146824563</span><span class="sxs-lookup"><span data-stu-id="066ff-148">-2146824563</span></span><br />
<span data-ttu-id="066ff-149">0x800A0E8D</span><span class="sxs-lookup"><span data-stu-id="066ff-149">0x800A0E8D</span></span></p></td>
<td><p><span data-ttu-id="066ff-150">No se puede establecer ni recuperar el valor de los datos porque el tipo de datos del campo era desconocido o el proveedor no tenía suficientes recursos para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="066ff-150">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-151"><strong>adErrCatalogNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-151"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-152">3747</span><span class="sxs-lookup"><span data-stu-id="066ff-152">3747</span></span><br />
<span data-ttu-id="066ff-153">-2146824541</span><span class="sxs-lookup"><span data-stu-id="066ff-153">-2146824541</span></span><br />
<span data-ttu-id="066ff-154">0x800A0EA3</span><span class="sxs-lookup"><span data-stu-id="066ff-154">0x800A0EA3</span></span></p></td>
<td><p><span data-ttu-id="066ff-155">La operación requiere un <strong>ParentCatalog</strong> válido.</span><span class="sxs-lookup"><span data-stu-id="066ff-155">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-156"><strong>adErrColumnNotOnThisRow</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-156"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-157">3726</span><span class="sxs-lookup"><span data-stu-id="066ff-157">3726</span></span><br />
<span data-ttu-id="066ff-158">-2146824562</span><span class="sxs-lookup"><span data-stu-id="066ff-158">-2146824562</span></span><br />
<span data-ttu-id="066ff-159">0x800A0E8E</span><span class="sxs-lookup"><span data-stu-id="066ff-159">0x800A0E8E</span></span></p></td>
<td><p><span data-ttu-id="066ff-160">El registro no contiene este campo.</span><span class="sxs-lookup"><span data-stu-id="066ff-160">Record does not contain this field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-161"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-161"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-162">3421</span><span class="sxs-lookup"><span data-stu-id="066ff-162">3421</span></span><br />
<span data-ttu-id="066ff-163">-2146824867</span><span class="sxs-lookup"><span data-stu-id="066ff-163">-2146824867</span></span><br />
<span data-ttu-id="066ff-164">0x800A0D5D</span><span class="sxs-lookup"><span data-stu-id="066ff-164">0x800A0D5D</span></span></p></td>
<td><p><span data-ttu-id="066ff-165">La aplicación utiliza un valor de tipo incorrecto para la operación actual.</span><span class="sxs-lookup"><span data-stu-id="066ff-165">Application uses a value of the wrong type for the current operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-166"><strong>adErrDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-166"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-167">3721</span><span class="sxs-lookup"><span data-stu-id="066ff-167">3721</span></span><br />
<span data-ttu-id="066ff-168">-2146824567</span><span class="sxs-lookup"><span data-stu-id="066ff-168">-2146824567</span></span><br />
<span data-ttu-id="066ff-169">0x800A0E89</span><span class="sxs-lookup"><span data-stu-id="066ff-169">0x800A0E89</span></span></p></td>
<td><p><span data-ttu-id="066ff-170">El valor de los datos es demasiado grande para poder representarlo mediante el tipo de datos del campo.</span><span class="sxs-lookup"><span data-stu-id="066ff-170">Data value is too large to be represented by the field data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-171"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-171"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-172">3738</span><span class="sxs-lookup"><span data-stu-id="066ff-172">3738</span></span><br />
<span data-ttu-id="066ff-173">-2146824550</span><span class="sxs-lookup"><span data-stu-id="066ff-173">-2146824550</span></span><br />
<span data-ttu-id="066ff-174">0x800A0E9A</span><span class="sxs-lookup"><span data-stu-id="066ff-174">0x800A0E9A</span></span></p></td>
<td><p><span data-ttu-id="066ff-175">La dirección URL del objeto que se va a eliminar está fuera del ámbito del registro actual.</span><span class="sxs-lookup"><span data-stu-id="066ff-175">URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-176"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-176"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-177">3750</span><span class="sxs-lookup"><span data-stu-id="066ff-177">3750</span></span><br />
<span data-ttu-id="066ff-178">-2146824538</span><span class="sxs-lookup"><span data-stu-id="066ff-178">-2146824538</span></span><br />
<span data-ttu-id="066ff-179">0x800A0EA6</span><span class="sxs-lookup"><span data-stu-id="066ff-179">0x800A0EA6</span></span></p></td>
<td><p><span data-ttu-id="066ff-180">El proveedor no admite restricciones compartidas.</span><span class="sxs-lookup"><span data-stu-id="066ff-180">Provider does not support sharing restrictions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-181"><strong>adErrDenyTypeNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-181"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-182">3751</span><span class="sxs-lookup"><span data-stu-id="066ff-182">3751</span></span><br />
<span data-ttu-id="066ff-183">-2146824537</span><span class="sxs-lookup"><span data-stu-id="066ff-183">-2146824537</span></span><br />
<span data-ttu-id="066ff-184">0x800A0EA7</span><span class="sxs-lookup"><span data-stu-id="066ff-184">0x800A0EA7</span></span></p></td>
<td><p><span data-ttu-id="066ff-185">El proveedor no admite el tipo restricciones compartidas solicitado.</span><span class="sxs-lookup"><span data-stu-id="066ff-185">Provider does not support the requested kind of sharing restriction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-186"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-186"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-187">3251</span><span class="sxs-lookup"><span data-stu-id="066ff-187">3251</span></span><br />
<span data-ttu-id="066ff-188">-2146825037</span><span class="sxs-lookup"><span data-stu-id="066ff-188">-2146825037</span></span><br />
<span data-ttu-id="066ff-189">0x800A0CB3</span><span class="sxs-lookup"><span data-stu-id="066ff-189">0x800A0CB3</span></span></p></td>
<td><p><span data-ttu-id="066ff-190">El objeto o el proveedor no es capaz de realizar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="066ff-190">Object or provider is not capable of performing requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-191"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-191"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-192">3749</span><span class="sxs-lookup"><span data-stu-id="066ff-192">3749</span></span><br />
<span data-ttu-id="066ff-193">-2146824539</span><span class="sxs-lookup"><span data-stu-id="066ff-193">-2146824539</span></span><br />
<span data-ttu-id="066ff-194">0x800A0EA5</span><span class="sxs-lookup"><span data-stu-id="066ff-194">0x800A0EA5</span></span></p></td>
<td><p><span data-ttu-id="066ff-p106">La actualización de campos no se realizó correctamente. Para obtener más información, examine la propiedad <strong>Status</strong> de cada objeto de campo.</span><span class="sxs-lookup"><span data-stu-id="066ff-p106">Fields update failed. For further information, examine the <strong>Status</strong> property of individual field objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-197"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-197"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-198">3219</span><span class="sxs-lookup"><span data-stu-id="066ff-198">3219</span></span><br />
<span data-ttu-id="066ff-199">-2146825069</span><span class="sxs-lookup"><span data-stu-id="066ff-199">-2146825069</span></span><br />
<span data-ttu-id="066ff-200">0x800A0C93</span><span class="sxs-lookup"><span data-stu-id="066ff-200">0x800A0C93</span></span></p></td>
<td><p><span data-ttu-id="066ff-201">Operación no permitida en este contexto.</span><span class="sxs-lookup"><span data-stu-id="066ff-201">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-202"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-202"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-203">3719</span><span class="sxs-lookup"><span data-stu-id="066ff-203">3719</span></span><br />
<span data-ttu-id="066ff-204">-2146824569</span><span class="sxs-lookup"><span data-stu-id="066ff-204">-2146824569</span></span><br />
<span data-ttu-id="066ff-205">0x800A0E87</span><span class="sxs-lookup"><span data-stu-id="066ff-205">0x800A0E87</span></span></p></td>
<td><p><span data-ttu-id="066ff-206">El valor de los datos entra en conflicto con las restricciones de integridad del campo.</span><span class="sxs-lookup"><span data-stu-id="066ff-206">Data value conflicts with the integrity constraints of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-207"><strong>adErrInTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-207"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-208">3246</span><span class="sxs-lookup"><span data-stu-id="066ff-208">3246</span></span><br />
<span data-ttu-id="066ff-209">-2146825042</span><span class="sxs-lookup"><span data-stu-id="066ff-209">-2146825042</span></span><br />
<span data-ttu-id="066ff-210">0x800A0CAE</span><span class="sxs-lookup"><span data-stu-id="066ff-210">0x800A0CAE</span></span></p></td>
<td><p><span data-ttu-id="066ff-211">No se puede cerrar explícitamente un objeto <strong>Connection</strong> durante una transacción.</span><span class="sxs-lookup"><span data-stu-id="066ff-211"><strong>Connection</strong> object cannot be explicitly closed while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-212"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-212"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-213">3001</span><span class="sxs-lookup"><span data-stu-id="066ff-213">3001</span></span><br />
<span data-ttu-id="066ff-214">-2146825287</span><span class="sxs-lookup"><span data-stu-id="066ff-214">-2146825287</span></span><br />
<span data-ttu-id="066ff-215">0x800A0BB9</span><span class="sxs-lookup"><span data-stu-id="066ff-215">0x800A0BB9</span></span></p></td>
<td><p><span data-ttu-id="066ff-216">Los argumentos son del tipo incorrecto, están fuera del intervalo aceptable o están en conflicto entre sí.</span><span class="sxs-lookup"><span data-stu-id="066ff-216">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-217"><strong>adErrInvalidConnection</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-217"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-218">3709</span><span class="sxs-lookup"><span data-stu-id="066ff-218">3709</span></span><br />
<span data-ttu-id="066ff-219">-2146824579</span><span class="sxs-lookup"><span data-stu-id="066ff-219">-2146824579</span></span><br />
<span data-ttu-id="066ff-220">0x800A0E7D</span><span class="sxs-lookup"><span data-stu-id="066ff-220">0x800A0E7D</span></span></p></td>
<td><p><span data-ttu-id="066ff-p107">No se puede utilizar la conexión para realizar esta operación. Está cerrada o no es válida en este contexto.</span><span class="sxs-lookup"><span data-stu-id="066ff-p107">The connection cannot be used to perform this operation. It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-223"><strong>adErrInvalidParamInfo</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-223"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-224">3708</span><span class="sxs-lookup"><span data-stu-id="066ff-224">3708</span></span><br />
<span data-ttu-id="066ff-225">-2146824580</span><span class="sxs-lookup"><span data-stu-id="066ff-225">-2146824580</span></span><br />
<span data-ttu-id="066ff-226">0x800A0E7C</span><span class="sxs-lookup"><span data-stu-id="066ff-226">0x800A0E7C</span></span></p></td>
<td><p><span data-ttu-id="066ff-p108">El objeto <strong>Parameter</strong> no se ha definido correctamente. Se proporcionó información incoherente o incompleta.  </span><span class="sxs-lookup"><span data-stu-id="066ff-p108"><strong>Parameter</strong> object is improperly defined. Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-229"><strong>adErrInvalidTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-229"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-230">3714</span><span class="sxs-lookup"><span data-stu-id="066ff-230">3714</span></span><br />
<span data-ttu-id="066ff-231">-2146824574</span><span class="sxs-lookup"><span data-stu-id="066ff-231">-2146824574</span></span><br />
<span data-ttu-id="066ff-232">0x800A0E82</span><span class="sxs-lookup"><span data-stu-id="066ff-232">0x800A0E82</span></span></p></td>
<td><p><span data-ttu-id="066ff-233">La transacción de coordinación no es válida o no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="066ff-233">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-234"><strong>adErrInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-234"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-235">3729</span><span class="sxs-lookup"><span data-stu-id="066ff-235">3729</span></span><br />
<span data-ttu-id="066ff-236">-2146824559</span><span class="sxs-lookup"><span data-stu-id="066ff-236">-2146824559</span></span><br />
<span data-ttu-id="066ff-237">0x800A0E91</span><span class="sxs-lookup"><span data-stu-id="066ff-237">0x800A0E91</span></span></p></td>
<td><p><span data-ttu-id="066ff-p109">La dirección URL contiene caracteres no válidos. Asegúrese de que la dirección URL está escrita correctamente.</span><span class="sxs-lookup"><span data-stu-id="066ff-p109">URL contains invalid characters. Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-240"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-240"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-241">3265</span><span class="sxs-lookup"><span data-stu-id="066ff-241">3265</span></span><br />
<span data-ttu-id="066ff-242">-2146825023</span><span class="sxs-lookup"><span data-stu-id="066ff-242">-2146825023</span></span><br />
<span data-ttu-id="066ff-243">0x800A0CC1</span><span class="sxs-lookup"><span data-stu-id="066ff-243">0x800A0CC1</span></span></p></td>
<td><p><span data-ttu-id="066ff-244">No se puede encontrar un elemento en la colección correspondiente al nombre o el ordinal solicitado.</span><span class="sxs-lookup"><span data-stu-id="066ff-244">Item cannot be found in the collection corresponding to the requested name or ordinal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-245"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-245"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-246">3021</span><span class="sxs-lookup"><span data-stu-id="066ff-246">3021</span></span><br />
<span data-ttu-id="066ff-247">-2146825267</span><span class="sxs-lookup"><span data-stu-id="066ff-247">-2146825267</span></span><br />
<span data-ttu-id="066ff-248">0x800A0BCD</span><span class="sxs-lookup"><span data-stu-id="066ff-248">0x800A0BCD</span></span></p></td>
<td><p><span data-ttu-id="066ff-p110"><strong>BOF</strong> o <strong>EOF</strong> es True o se ha eliminado el registro actual. La operación solicitada requiere un registro actual.</span><span class="sxs-lookup"><span data-stu-id="066ff-p110">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted. Requested operation requires a current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-251"><strong>adErrNotExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-251"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-252">3715</span><span class="sxs-lookup"><span data-stu-id="066ff-252">3715</span></span><br />
<span data-ttu-id="066ff-253">-2146824573</span><span class="sxs-lookup"><span data-stu-id="066ff-253">-2146824573</span></span><br />
<span data-ttu-id="066ff-254">0x800A0E83</span><span class="sxs-lookup"><span data-stu-id="066ff-254">0x800A0E83</span></span></p></td>
<td><p><span data-ttu-id="066ff-255">No se puede realizar la operación mientras no se ejecute.</span><span class="sxs-lookup"><span data-stu-id="066ff-255">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-256"><strong>adErrNotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-256"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-257">3710</span><span class="sxs-lookup"><span data-stu-id="066ff-257">3710</span></span><br />
<span data-ttu-id="066ff-258">-2146824578</span><span class="sxs-lookup"><span data-stu-id="066ff-258">-2146824578</span></span><br />
<span data-ttu-id="066ff-259">0x800A0E7E</span><span class="sxs-lookup"><span data-stu-id="066ff-259">0x800A0E7E</span></span></p></td>
<td><p><span data-ttu-id="066ff-260">No se puede realizar la operación mientras se procesa el evento.</span><span class="sxs-lookup"><span data-stu-id="066ff-260">Operation cannot be performed while processing event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-261"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-261"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-262">3704</span><span class="sxs-lookup"><span data-stu-id="066ff-262">3704</span></span><br />
<span data-ttu-id="066ff-263">-2146824584</span><span class="sxs-lookup"><span data-stu-id="066ff-263">-2146824584</span></span><br />
<span data-ttu-id="066ff-264">0x800A0E78</span><span class="sxs-lookup"><span data-stu-id="066ff-264">0x800A0E78</span></span></p></td>
<td><p><span data-ttu-id="066ff-265">La operación no está permitida si el objeto está cerrado.</span><span class="sxs-lookup"><span data-stu-id="066ff-265">Operation is not allowed when the object is closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-266"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-266"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-267">3367</span><span class="sxs-lookup"><span data-stu-id="066ff-267">3367</span></span><br />
<span data-ttu-id="066ff-268">-2146824921</span><span class="sxs-lookup"><span data-stu-id="066ff-268">-2146824921</span></span><br />
<span data-ttu-id="066ff-269">0x800A0D27</span><span class="sxs-lookup"><span data-stu-id="066ff-269">0x800A0D27</span></span></p></td>
<td><p><span data-ttu-id="066ff-p111">El objeto ya está en la colección. No se puede anexar.</span><span class="sxs-lookup"><span data-stu-id="066ff-p111">Object is already in collection. Cannot append.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-272"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-272"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-273">3420</span><span class="sxs-lookup"><span data-stu-id="066ff-273">3420</span></span><br />
<span data-ttu-id="066ff-274">-2146824868</span><span class="sxs-lookup"><span data-stu-id="066ff-274">-2146824868</span></span><br />
<span data-ttu-id="066ff-275">0x800A0D5C</span><span class="sxs-lookup"><span data-stu-id="066ff-275">0x800A0D5C</span></span></p></td>
<td><p><span data-ttu-id="066ff-276">El objeto ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="066ff-276">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-277"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-277"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-278">3705</span><span class="sxs-lookup"><span data-stu-id="066ff-278">3705</span></span><br />
<span data-ttu-id="066ff-279">-2146824583</span><span class="sxs-lookup"><span data-stu-id="066ff-279">-2146824583</span></span><br />
<span data-ttu-id="066ff-280">0x800A0E79</span><span class="sxs-lookup"><span data-stu-id="066ff-280">0x800A0E79</span></span></p></td>
<td><p><span data-ttu-id="066ff-281">La operación no está permitida si el objeto está abierto.</span><span class="sxs-lookup"><span data-stu-id="066ff-281">Operation is not allowed when the object is open.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-282"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-282"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-283">3002</span><span class="sxs-lookup"><span data-stu-id="066ff-283">3002</span></span><br />
<span data-ttu-id="066ff-284">-2146825286</span><span class="sxs-lookup"><span data-stu-id="066ff-284">-2146825286</span></span><br />
<span data-ttu-id="066ff-285">0x800A0BBA</span><span class="sxs-lookup"><span data-stu-id="066ff-285">0x800A0BBA</span></span></p></td>
<td><p><span data-ttu-id="066ff-286">No se pudo abrir un archivo.</span><span class="sxs-lookup"><span data-stu-id="066ff-286">File could not be opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-287"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-287"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-288">3712</span><span class="sxs-lookup"><span data-stu-id="066ff-288">3712</span></span><br />
<span data-ttu-id="066ff-289">-2146824576</span><span class="sxs-lookup"><span data-stu-id="066ff-289">-2146824576</span></span><br />
<span data-ttu-id="066ff-290">0x800A0E80</span><span class="sxs-lookup"><span data-stu-id="066ff-290">0x800A0E80</span></span></p></td>
<td><p><span data-ttu-id="066ff-291">La operación ha sido cancelada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="066ff-291">Operation has been cancelled by the user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-292"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-292"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-293">3734</span><span class="sxs-lookup"><span data-stu-id="066ff-293">3734</span></span><br />
<span data-ttu-id="066ff-294">-2146824554</span><span class="sxs-lookup"><span data-stu-id="066ff-294">-2146824554</span></span><br />
<span data-ttu-id="066ff-295">0x800A0E96</span><span class="sxs-lookup"><span data-stu-id="066ff-295">0x800A0E96</span></span></p></td>
<td><p><span data-ttu-id="066ff-p112">No se puede realizar la operación. El proveedor no puede obtener suficiente espacio de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="066ff-p112">Operation cannot be performed. Provider cannot obtain enough storage space.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-298"><strong>adErrPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-298"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-299">3720</span><span class="sxs-lookup"><span data-stu-id="066ff-299">3720</span></span><br />
<span data-ttu-id="066ff-300">-2146824568</span><span class="sxs-lookup"><span data-stu-id="066ff-300">-2146824568</span></span><br />
<span data-ttu-id="066ff-301">0x800A0E88</span><span class="sxs-lookup"><span data-stu-id="066ff-301">0x800A0E88</span></span></p></td>
<td><p><span data-ttu-id="066ff-302">La falta de permiso suficiente impide escribir en el campo.</span><span class="sxs-lookup"><span data-stu-id="066ff-302">Insufficent permission prevents writing to the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-303"><strong>adErrProviderFailed</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-303"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-304">3000</span><span class="sxs-lookup"><span data-stu-id="066ff-304">3000</span></span><br />
<span data-ttu-id="066ff-305">-2146825288</span><span class="sxs-lookup"><span data-stu-id="066ff-305">-2146825288</span></span><br />
<span data-ttu-id="066ff-306">0x800A0BB8</span><span class="sxs-lookup"><span data-stu-id="066ff-306">0x800A0BB8</span></span></p></td>
<td><p><span data-ttu-id="066ff-307">El proveedor no pudo realizar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="066ff-307">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-308"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-308"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-309">3706</span><span class="sxs-lookup"><span data-stu-id="066ff-309">3706</span></span><br />
<span data-ttu-id="066ff-310">-2146824582</span><span class="sxs-lookup"><span data-stu-id="066ff-310">-2146824582</span></span><br />
<span data-ttu-id="066ff-311">0x800A0E7A</span><span class="sxs-lookup"><span data-stu-id="066ff-311">0x800A0E7A</span></span></p></td>
<td><p><span data-ttu-id="066ff-p113">No se puede encontrar un proveedor.Es posible que no se haya instalado correctamente.</span><span class="sxs-lookup"><span data-stu-id="066ff-p113">Provider cannot be found. It may not be properly installed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-314"><strong>adErrReadFile</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-314"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-315">3003</span><span class="sxs-lookup"><span data-stu-id="066ff-315">3003</span></span><br />
<span data-ttu-id="066ff-316">-2146825285</span><span class="sxs-lookup"><span data-stu-id="066ff-316">-2146825285</span></span><br />
<span data-ttu-id="066ff-317">0x800A0BBB</span><span class="sxs-lookup"><span data-stu-id="066ff-317">0x800A0BBB</span></span></p></td>
<td><p><span data-ttu-id="066ff-318">No se pudo leer un archivo.</span><span class="sxs-lookup"><span data-stu-id="066ff-318">File could not be read.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-319"><strong>adErrResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-319"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-320">3731</span><span class="sxs-lookup"><span data-stu-id="066ff-320">3731</span></span><br />
<span data-ttu-id="066ff-321">-2146824557</span><span class="sxs-lookup"><span data-stu-id="066ff-321">-2146824557</span></span><br />
<span data-ttu-id="066ff-322">0x800A0E93</span><span class="sxs-lookup"><span data-stu-id="066ff-322">0x800A0E93</span></span></p></td>
<td><p><span data-ttu-id="066ff-p114">No se puede realizar la operación de copia. El objeto denominado por la dirección URL de destino ya existe. Especifique <strong>adCopyOverwrite</strong> para reemplazar el objeto.</span><span class="sxs-lookup"><span data-stu-id="066ff-p114">Copy operation cannot be performed. Object named by destination URL already exists. Specify <strong>adCopyOverwrite</strong> to replace the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-326"><strong>adErrResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-326"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-327">3730</span><span class="sxs-lookup"><span data-stu-id="066ff-327">3730</span></span><br />
<span data-ttu-id="066ff-328">-2146824558</span><span class="sxs-lookup"><span data-stu-id="066ff-328">-2146824558</span></span><br />
<span data-ttu-id="066ff-329">0x800A0E92</span><span class="sxs-lookup"><span data-stu-id="066ff-329">0x800A0E92</span></span></p></td>
<td><p><span data-ttu-id="066ff-p115">Un objeto representado por la dirección URL especificada está bloqueado por uno o más procesos. Espere hasta que el proceso haya finalizado e intente de nuevo la operación.</span><span class="sxs-lookup"><span data-stu-id="066ff-p115">Object represented by the specified URL is locked by one or more other processes. Wait until the process has finished and attempt the operation again.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-332"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-332"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-333">3735</span><span class="sxs-lookup"><span data-stu-id="066ff-333">3735</span></span><br />
<span data-ttu-id="066ff-334">-2146824553</span><span class="sxs-lookup"><span data-stu-id="066ff-334">-2146824553</span></span><br />
<span data-ttu-id="066ff-335">0x800A0E97</span><span class="sxs-lookup"><span data-stu-id="066ff-335">0x800A0E97</span></span></p></td>
<td><p><span data-ttu-id="066ff-336">La dirección URL de origen o de destino está fuera del alcance del registro activo.</span><span class="sxs-lookup"><span data-stu-id="066ff-336">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-337"><strong>adErrSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-337"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-338">3722</span><span class="sxs-lookup"><span data-stu-id="066ff-338">3722</span></span><br />
<span data-ttu-id="066ff-339">-2146824566</span><span class="sxs-lookup"><span data-stu-id="066ff-339">-2146824566</span></span><br />
<span data-ttu-id="066ff-340">0x800A0E8A</span><span class="sxs-lookup"><span data-stu-id="066ff-340">0x800A0E8A</span></span></p></td>
<td><p><span data-ttu-id="066ff-341">El valor de los datos está en conflicto con el tipo de datos o las restricciones del campo.</span><span class="sxs-lookup"><span data-stu-id="066ff-341">Data value conflicts with the data type or constraints of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-342"><strong>adErrSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-342"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-343">3723</span><span class="sxs-lookup"><span data-stu-id="066ff-343">3723</span></span><br />
<span data-ttu-id="066ff-344">-2146824565</span><span class="sxs-lookup"><span data-stu-id="066ff-344">-2146824565</span></span><br />
<span data-ttu-id="066ff-345">0x800A0E8B</span><span class="sxs-lookup"><span data-stu-id="066ff-345">0x800A0E8B</span></span></p></td>
<td><p><span data-ttu-id="066ff-346">La conversión produjo un error porque el valor de los datos tenía signo y el tipo de datos del campo utilizado por el proveedor no tenía signo.</span><span class="sxs-lookup"><span data-stu-id="066ff-346">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-347"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-347"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-348">3713</span><span class="sxs-lookup"><span data-stu-id="066ff-348">3713</span></span><br />
<span data-ttu-id="066ff-349">-2146824575</span><span class="sxs-lookup"><span data-stu-id="066ff-349">-2146824575</span></span><br />
<span data-ttu-id="066ff-350">0x800A0E81</span><span class="sxs-lookup"><span data-stu-id="066ff-350">0x800A0E81</span></span></p></td>
<td><p><span data-ttu-id="066ff-351">No se puede realizar la operación mientras se conecta asincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="066ff-351">Operation cannot be performed while connecting aynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-352"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-352"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-353">3711</span><span class="sxs-lookup"><span data-stu-id="066ff-353">3711</span></span><br />
<span data-ttu-id="066ff-354">-2146824577</span><span class="sxs-lookup"><span data-stu-id="066ff-354">-2146824577</span></span><br />
<span data-ttu-id="066ff-355">0x800A0E7F</span><span class="sxs-lookup"><span data-stu-id="066ff-355">0x800A0E7F</span></span></p></td>
<td><p><span data-ttu-id="066ff-356">No se puede realizar la operación mientras se ejecuta asincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="066ff-356">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-357"><strong>adErrTreePermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-357"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-358">3728</span><span class="sxs-lookup"><span data-stu-id="066ff-358">3728</span></span><br />
<span data-ttu-id="066ff-359">-2146824560</span><span class="sxs-lookup"><span data-stu-id="066ff-359">-2146824560</span></span><br />
<span data-ttu-id="066ff-360">0x800A0E90</span><span class="sxs-lookup"><span data-stu-id="066ff-360">0x800A0E90</span></span></p></td>
<td><p><span data-ttu-id="066ff-361">No se tienen suficientes permisos para obtener acceso a un árbol o a un subárbol.</span><span class="sxs-lookup"><span data-stu-id="066ff-361">Permissions are insufficient to access tree or subtree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-362"><strong>adErrUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-362"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-363">3736</span><span class="sxs-lookup"><span data-stu-id="066ff-363">3736</span></span><br />
<span data-ttu-id="066ff-364">-2146824552</span><span class="sxs-lookup"><span data-stu-id="066ff-364">-2146824552</span></span><br />
<span data-ttu-id="066ff-365">0x800A0E98</span><span class="sxs-lookup"><span data-stu-id="066ff-365">0x800A0E98</span></span></p></td>
<td><p><span data-ttu-id="066ff-p116">La operación no se pudo completar y el estado no está disponible. El campo puede no estar disponible o no se intentó la operación.</span><span class="sxs-lookup"><span data-stu-id="066ff-p116">Operation failed to complete and the status is unavailable. The field may be unavailable or the operation was not attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-368"><strong>adErrUnsafeOperation</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-368"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-369">3716</span><span class="sxs-lookup"><span data-stu-id="066ff-369">3716</span></span><br />
<span data-ttu-id="066ff-370">-2146824572</span><span class="sxs-lookup"><span data-stu-id="066ff-370">-2146824572</span></span><br />
<span data-ttu-id="066ff-371">0x800A0E84</span><span class="sxs-lookup"><span data-stu-id="066ff-371">0x800A0E84</span></span></p></td>
<td><p><span data-ttu-id="066ff-372">La configuración de seguridad de este equipo prohíbe el acceso a un origen de datos en otro dominio.</span><span class="sxs-lookup"><span data-stu-id="066ff-372">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-373"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-373"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-374">3727</span><span class="sxs-lookup"><span data-stu-id="066ff-374">3727</span></span><br />
<span data-ttu-id="066ff-375">-2146824561</span><span class="sxs-lookup"><span data-stu-id="066ff-375">-2146824561</span></span><br />
<span data-ttu-id="066ff-376">0x800A0E8F</span><span class="sxs-lookup"><span data-stu-id="066ff-376">0x800A0E8F</span></span></p></td>
<td><p><span data-ttu-id="066ff-377">No existe la dirección URL de origen o la dirección URL del elemento principal de destino.</span><span class="sxs-lookup"><span data-stu-id="066ff-377">Either the source URL or the parent of the destination URL does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-378"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-378"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-379">3737</span><span class="sxs-lookup"><span data-stu-id="066ff-379">3737</span></span><br />
<span data-ttu-id="066ff-380">-2146824551</span><span class="sxs-lookup"><span data-stu-id="066ff-380">-2146824551</span></span><br />
<span data-ttu-id="066ff-381">0x800A0E99</span><span class="sxs-lookup"><span data-stu-id="066ff-381">0x800A0E99</span></span></p></td>
<td><p><span data-ttu-id="066ff-382">No existe el registro mencionado en esta dirección URL.</span><span class="sxs-lookup"><span data-stu-id="066ff-382">Record named by this URL does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-383"><strong>adErrVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-383"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-384">3733</span><span class="sxs-lookup"><span data-stu-id="066ff-384">3733</span></span><br />
<span data-ttu-id="066ff-385">-2146824555</span><span class="sxs-lookup"><span data-stu-id="066ff-385">-2146824555</span></span><br />
<span data-ttu-id="066ff-386">0x800A0E95</span><span class="sxs-lookup"><span data-stu-id="066ff-386">0x800A0E95</span></span></p></td>
<td><p><span data-ttu-id="066ff-p117">El proveedor no puede encontrar el dispositivo de almacenamiento indicado por la dirección URL. Asegúrese de que la dirección URL está escrita correctamente.</span><span class="sxs-lookup"><span data-stu-id="066ff-p117">Provider cannot locate the storage device indicated by the URL. Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-389"><strong>adErrWriteFile</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-389"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-390">3004</span><span class="sxs-lookup"><span data-stu-id="066ff-390">3004</span></span><br />
<span data-ttu-id="066ff-391">-2146825284</span><span class="sxs-lookup"><span data-stu-id="066ff-391">-2146825284</span></span><br />
<span data-ttu-id="066ff-392">0x800A0BBC</span><span class="sxs-lookup"><span data-stu-id="066ff-392">0x800A0BBC</span></span></p></td>
<td><p><span data-ttu-id="066ff-393">Error de escritura en un archivo.</span><span class="sxs-lookup"><span data-stu-id="066ff-393">Write to file failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-394"><strong>adWrnSecurityDialog</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-394"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-395">3717</span><span class="sxs-lookup"><span data-stu-id="066ff-395">3717</span></span><br />
<span data-ttu-id="066ff-396">-2146824571</span><span class="sxs-lookup"><span data-stu-id="066ff-396">-2146824571</span></span><br />
<span data-ttu-id="066ff-397">0x800A0E85</span><span class="sxs-lookup"><span data-stu-id="066ff-397">0x800A0E85</span></span></p></td>
<td><p><span data-ttu-id="066ff-p118">Sólo para uso interno. No la utilice.</span><span class="sxs-lookup"><span data-stu-id="066ff-p118">For internal use only. Don't use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-400"><strong>adWrnSecurityDialogHeader</strong></span><span class="sxs-lookup"><span data-stu-id="066ff-400"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="066ff-401">3718</span><span class="sxs-lookup"><span data-stu-id="066ff-401">3718</span></span><br />
<span data-ttu-id="066ff-402">-2146824570</span><span class="sxs-lookup"><span data-stu-id="066ff-402">-2146824570</span></span><br />
<span data-ttu-id="066ff-403">0x800A0E86</span><span class="sxs-lookup"><span data-stu-id="066ff-403">0x800A0E86</span></span></p></td>
<td><p><span data-ttu-id="066ff-p119">Sólo para uso interno. No la utilice.</span><span class="sxs-lookup"><span data-stu-id="066ff-p119">For internal use only. Don't use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="066ff-406">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="066ff-406">ADO/WFC equivalent</span></span>

<span data-ttu-id="066ff-407">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="066ff-407">Package: **com.ms.wfc.data**</span></span>

<span data-ttu-id="066ff-408">Se definen sólo los subconjuntos siguientes de equivalentes ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="066ff-408">Only the following subsets of ADO/WFC equivalents are defined.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="066ff-409">Constante</span><span class="sxs-lookup"><span data-stu-id="066ff-409">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="066ff-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span><span class="sxs-lookup"><span data-stu-id="066ff-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-411">AdoEnums.ErrorValue.DATACONVERSION</span><span class="sxs-lookup"><span data-stu-id="066ff-411">AdoEnums.ErrorValue.DATACONVERSION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="066ff-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span><span class="sxs-lookup"><span data-stu-id="066ff-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-414">AdoEnums.ErrorValue.INTRANSACTION</span><span class="sxs-lookup"><span data-stu-id="066ff-414">AdoEnums.ErrorValue.INTRANSACTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span><span class="sxs-lookup"><span data-stu-id="066ff-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span><span class="sxs-lookup"><span data-stu-id="066ff-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span><span class="sxs-lookup"><span data-stu-id="066ff-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="066ff-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span><span class="sxs-lookup"><span data-stu-id="066ff-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-420">AdoEnums.ErrorValue.NOTEXECUTING</span><span class="sxs-lookup"><span data-stu-id="066ff-420">AdoEnums.ErrorValue.NOTEXECUTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-421">AdoEnums.ErrorValue.NOTREENTRANT</span><span class="sxs-lookup"><span data-stu-id="066ff-421">AdoEnums.ErrorValue.NOTREENTRANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-422">AdoEnums.ErrorValue.OBJECTCLOSED</span><span class="sxs-lookup"><span data-stu-id="066ff-422">AdoEnums.ErrorValue.OBJECTCLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="066ff-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-424">AdoEnums.ErrorValue.OBJECTNOTSET</span><span class="sxs-lookup"><span data-stu-id="066ff-424">AdoEnums.ErrorValue.OBJECTNOTSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-425">AdoEnums.ErrorValue.OBJECTOPEN</span><span class="sxs-lookup"><span data-stu-id="066ff-425">AdoEnums.ErrorValue.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span><span class="sxs-lookup"><span data-stu-id="066ff-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="066ff-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-428">AdoEnums.ErrorValue.STILLCONNECTING</span><span class="sxs-lookup"><span data-stu-id="066ff-428">AdoEnums.ErrorValue.STILLCONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066ff-429">AdoEnums.ErrorValue.STILLEXECUTING</span><span class="sxs-lookup"><span data-stu-id="066ff-429">AdoEnums.ErrorValue.STILLEXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066ff-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span><span class="sxs-lookup"><span data-stu-id="066ff-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span></span></p></td>
</tr>
</tbody>
</table>

