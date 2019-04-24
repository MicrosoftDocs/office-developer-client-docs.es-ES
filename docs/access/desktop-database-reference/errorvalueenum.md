---
title: ErrorValueEnum (referencia de base de datos de escritorio de Access)
TOCTitle: ErrorValueEnum
ms:assetid: 2af99f32-6004-1225-367c-45d693f447b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249058(v=office.15)
ms:contentKeyID: 48543921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c2d4207f157d361f3b8aba2ff80f46d06b2f328e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293325"
---
# <a name="errorvalueenum"></a><span data-ttu-id="a42bd-102">ErrorValueEnum</span><span class="sxs-lookup"><span data-stu-id="a42bd-102">ErrorValueEnum</span></span>

<span data-ttu-id="a42bd-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a42bd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a42bd-104">Especifica el tipo de error ADO en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="a42bd-104">Specifies the type of ADO run-time error.</span></span>

<span data-ttu-id="a42bd-105">Se muestran tres formas del número de error:</span><span class="sxs-lookup"><span data-stu-id="a42bd-105">Three forms of the error number are listed:</span></span>

- <span data-ttu-id="a42bd-p101">Decimal positivo: los dos bytes bajos del número completo en formato decimal. Este número aparece en el cuadro de diálogo predeterminado de mensaje de error de Visual Basic. Por ejemplo, Error en tiempo de ejecución "3707".</span><span class="sxs-lookup"><span data-stu-id="a42bd-p101">Positive decimal — the low two bytes of the full number in decimal format. This number is displayed in the default Visual Basic error message dialog box. For example, Run-time error '3707'.</span></span>

- <span data-ttu-id="a42bd-109">Decimal negativo: la traducción decimal del número de error completo.</span><span class="sxs-lookup"><span data-stu-id="a42bd-109">Negative decimal — The decimal translation of the full error number.</span></span>

- <span data-ttu-id="a42bd-110">Hexadecimal: la representación hexadecimal del número de error completo.</span><span class="sxs-lookup"><span data-stu-id="a42bd-110">Hexadecimal — The hexadecimal representation of the full error number.</span></span> <span data-ttu-id="a42bd-111">El código de servicio de Windows se encuentra en el cuarto dígito.</span><span class="sxs-lookup"><span data-stu-id="a42bd-111">The Windows facility code is in the fourth digit.</span></span> <span data-ttu-id="a42bd-112">El código de servicio para los números de error ADO es *un*. Por ejemplo: 0x800***A***0E7B.</span><span class="sxs-lookup"><span data-stu-id="a42bd-112">The facility code for ADO error numbers is *A*. For example: 0x800***A***0E7B.</span></span>

> [!NOTE]
> <span data-ttu-id="a42bd-113">Los errores OLE DB se pueden pasar a una aplicación ADO.</span><span class="sxs-lookup"><span data-stu-id="a42bd-113">OLE DB errors may be passed to your ADO application.</span></span> <span data-ttu-id="a42bd-114">Éstos, normalmente, se pueden identificar por un código de servicio de Windows de *4* dígitos.</span><span class="sxs-lookup"><span data-stu-id="a42bd-114">Typically, these can be identified by a Windows facility code of *4*.</span></span> <span data-ttu-id="a42bd-115">Por ejemplo, 0x800_**4**_.... Para obtener más información acerca de estos números, vea el capítulo 16 de la *Referencia del programador de OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="a42bd-115">For example, 0x800_**4**_.... For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a42bd-116">Constante</span><span class="sxs-lookup"><span data-stu-id="a42bd-116">Constant</span></span></p></th>
<th><p><span data-ttu-id="a42bd-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a42bd-117">Value</span></span></p></th>
<th><p><span data-ttu-id="a42bd-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a42bd-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-119"><strong>adErrBoundToCommand</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-119"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-120">3707</span><span class="sxs-lookup"><span data-stu-id="a42bd-120">3707</span></span><br />
<span data-ttu-id="a42bd-121">-2146824581</span><span class="sxs-lookup"><span data-stu-id="a42bd-121">-2146824581</span></span><br />
<span data-ttu-id="a42bd-122">0x800A0E7B</span><span class="sxs-lookup"><span data-stu-id="a42bd-122">0x800A0E7B</span></span></p></td>
<td><p><span data-ttu-id="a42bd-123">No se puede cambiar la propiedad <strong>ActiveConnection</strong> de un objeto <strong>Recordset</strong> que tiene un objeto <strong>Command</strong> como su origen.</span><span class="sxs-lookup"><span data-stu-id="a42bd-123">Cannot change the <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object which has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-124"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-124"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-125">3732</span><span class="sxs-lookup"><span data-stu-id="a42bd-125">3732</span></span><br />
<span data-ttu-id="a42bd-126">-2146824556</span><span class="sxs-lookup"><span data-stu-id="a42bd-126">-2146824556</span></span><br />
<span data-ttu-id="a42bd-127">0x800A0E94</span><span class="sxs-lookup"><span data-stu-id="a42bd-127">0x800A0E94</span></span></p></td>
<td><p><span data-ttu-id="a42bd-128">El servidor no puede completar la operación.</span><span class="sxs-lookup"><span data-stu-id="a42bd-128">Server cannot complete the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-129"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-129"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-130">3748</span><span class="sxs-lookup"><span data-stu-id="a42bd-130">3748</span></span><br />
<span data-ttu-id="a42bd-131">-2146824540</span><span class="sxs-lookup"><span data-stu-id="a42bd-131">-2146824540</span></span><br />
<span data-ttu-id="a42bd-132">0x800A0EA4</span><span class="sxs-lookup"><span data-stu-id="a42bd-132">0x800A0EA4</span></span></p></td>
<td><p><span data-ttu-id="a42bd-133">Se denegó conexión.</span><span class="sxs-lookup"><span data-stu-id="a42bd-133">Connection was denied.</span></span> <span data-ttu-id="a42bd-134">La conexión nueva que solicitó tiene características diferentes de la que ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="a42bd-134">New connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-135"><strong>adErrCantChangeProvider</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-135"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-136">3220</span><span class="sxs-lookup"><span data-stu-id="a42bd-136">3220</span></span><br />
<span data-ttu-id="a42bd-137">-2146825068</span><span class="sxs-lookup"><span data-stu-id="a42bd-137">-2146825068</span></span><br />
<span data-ttu-id="a42bd-138">0X800A0C94</span><span class="sxs-lookup"><span data-stu-id="a42bd-138">0X800A0C94</span></span></p></td>
<td><p><span data-ttu-id="a42bd-139">El proveedor suministrado es distinto del que se está utilizando.</span><span class="sxs-lookup"><span data-stu-id="a42bd-139">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-140"><strong>adErrCantConvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-140"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-141">3724</span><span class="sxs-lookup"><span data-stu-id="a42bd-141">3724</span></span><br />
<span data-ttu-id="a42bd-142">-2146824564</span><span class="sxs-lookup"><span data-stu-id="a42bd-142">-2146824564</span></span><br />
<span data-ttu-id="a42bd-143">0x800A0E8C</span><span class="sxs-lookup"><span data-stu-id="a42bd-143">0x800A0E8C</span></span></p></td>
<td><p><span data-ttu-id="a42bd-144">El valor de los datos no se puede convertir por motivos distintos a un desajuste entre signos o a un desbordamiento de datos.</span><span class="sxs-lookup"><span data-stu-id="a42bd-144">Data value cannot be converted for reasons other than sign mismatch or data overflow.</span></span> <span data-ttu-id="a42bd-145">Por ejemplo, la conversión habría truncado los datos.</span><span class="sxs-lookup"><span data-stu-id="a42bd-145">For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-146"><strong>adErrCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-146"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-147">3725</span><span class="sxs-lookup"><span data-stu-id="a42bd-147">3725</span></span><br />
<span data-ttu-id="a42bd-148">-2146824563</span><span class="sxs-lookup"><span data-stu-id="a42bd-148">-2146824563</span></span><br />
<span data-ttu-id="a42bd-149">0x800A0E8D</span><span class="sxs-lookup"><span data-stu-id="a42bd-149">0x800A0E8D</span></span></p></td>
<td><p><span data-ttu-id="a42bd-150">El valor de los datos no se puede establecer o recuperar porque el tipo de datos del campo era desconocido o el proveedor no dispuso de recursos suficientes para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="a42bd-150">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-151"><strong>adErrCatalogNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-151"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-152">3747</span><span class="sxs-lookup"><span data-stu-id="a42bd-152">3747</span></span><br />
<span data-ttu-id="a42bd-153">-2146824541</span><span class="sxs-lookup"><span data-stu-id="a42bd-153">-2146824541</span></span><br />
<span data-ttu-id="a42bd-154">0x800A0EA3</span><span class="sxs-lookup"><span data-stu-id="a42bd-154">0x800A0EA3</span></span></p></td>
<td><p><span data-ttu-id="a42bd-155">La operación requiere un <strong>ParentCatalog</strong> válido.</span><span class="sxs-lookup"><span data-stu-id="a42bd-155">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-156"><strong>adErrColumnNotOnThisRow</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-156"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-157">3726</span><span class="sxs-lookup"><span data-stu-id="a42bd-157">3726</span></span><br />
<span data-ttu-id="a42bd-158">-2146824562</span><span class="sxs-lookup"><span data-stu-id="a42bd-158">-2146824562</span></span><br />
<span data-ttu-id="a42bd-159">0x800A0E8E</span><span class="sxs-lookup"><span data-stu-id="a42bd-159">0x800A0E8E</span></span></p></td>
<td><p><span data-ttu-id="a42bd-160">El registro no contiene este campo.</span><span class="sxs-lookup"><span data-stu-id="a42bd-160">Record does not contain this field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-161"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-161"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-162">3421</span><span class="sxs-lookup"><span data-stu-id="a42bd-162">3421</span></span><br />
<span data-ttu-id="a42bd-163">-2146824867</span><span class="sxs-lookup"><span data-stu-id="a42bd-163">-2146824867</span></span><br />
<span data-ttu-id="a42bd-164">0x800A0D5D</span><span class="sxs-lookup"><span data-stu-id="a42bd-164">0x800A0D5D</span></span></p></td>
<td><p><span data-ttu-id="a42bd-165">La aplicación utiliza un valor de tipo no válido para la operación actual.</span><span class="sxs-lookup"><span data-stu-id="a42bd-165">Application uses a value of the wrong type for the current operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-166"><strong>adErrDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-166"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-167">3721</span><span class="sxs-lookup"><span data-stu-id="a42bd-167">3721</span></span><br />
<span data-ttu-id="a42bd-168">-2146824567</span><span class="sxs-lookup"><span data-stu-id="a42bd-168">-2146824567</span></span><br />
<span data-ttu-id="a42bd-169">0x800A0E89</span><span class="sxs-lookup"><span data-stu-id="a42bd-169">0x800A0E89</span></span></p></td>
<td><p><span data-ttu-id="a42bd-170">El valor de los datos es demasiado grande para ser representado por el tipo de datos del campo.</span><span class="sxs-lookup"><span data-stu-id="a42bd-170">Data value is too large to be represented by the field data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-171"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-171"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-172">3738</span><span class="sxs-lookup"><span data-stu-id="a42bd-172">3738</span></span><br />
<span data-ttu-id="a42bd-173">-2146824550</span><span class="sxs-lookup"><span data-stu-id="a42bd-173">-2146824550</span></span><br />
<span data-ttu-id="a42bd-174">0x800A0E9A</span><span class="sxs-lookup"><span data-stu-id="a42bd-174">0x800A0E9A</span></span></p></td>
<td><p><span data-ttu-id="a42bd-175">La dirección URL del objeto que se va a eliminar está fuera del ámbito del registro actual.</span><span class="sxs-lookup"><span data-stu-id="a42bd-175">URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-176"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-176"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-177">3750</span><span class="sxs-lookup"><span data-stu-id="a42bd-177">3750</span></span><br />
<span data-ttu-id="a42bd-178">-2146824538</span><span class="sxs-lookup"><span data-stu-id="a42bd-178">-2146824538</span></span><br />
<span data-ttu-id="a42bd-179">0x800A0EA6</span><span class="sxs-lookup"><span data-stu-id="a42bd-179">0x800A0EA6</span></span></p></td>
<td><p><span data-ttu-id="a42bd-180">El proveedor no admite restricciones compartidas.</span><span class="sxs-lookup"><span data-stu-id="a42bd-180">Provider does not support sharing restrictions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-181"><strong>adErrDenyTypeNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-181"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-182">3751</span><span class="sxs-lookup"><span data-stu-id="a42bd-182">3751</span></span><br />
<span data-ttu-id="a42bd-183">-2146824537</span><span class="sxs-lookup"><span data-stu-id="a42bd-183">-2146824537</span></span><br />
<span data-ttu-id="a42bd-184">0x800A0EA7</span><span class="sxs-lookup"><span data-stu-id="a42bd-184">0x800A0EA7</span></span></p></td>
<td><p><span data-ttu-id="a42bd-185">El proveedor no admite el tipo solicitado de restricción compartida.</span><span class="sxs-lookup"><span data-stu-id="a42bd-185">Provider does not support the requested kind of sharing restriction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-186"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-186"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-187">3251</span><span class="sxs-lookup"><span data-stu-id="a42bd-187">3251</span></span><br />
<span data-ttu-id="a42bd-188">-2146825037</span><span class="sxs-lookup"><span data-stu-id="a42bd-188">-2146825037</span></span><br />
<span data-ttu-id="a42bd-189">0x800A0CB3</span><span class="sxs-lookup"><span data-stu-id="a42bd-189">0x800A0CB3</span></span></p></td>
<td><p><span data-ttu-id="a42bd-190">El objeto o el proveedor no es capaz de realizar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="a42bd-190">Object or provider is not capable of performing requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-191"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-191"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-192">3749</span><span class="sxs-lookup"><span data-stu-id="a42bd-192">3749</span></span><br />
<span data-ttu-id="a42bd-193">-2146824539</span><span class="sxs-lookup"><span data-stu-id="a42bd-193">-2146824539</span></span><br />
<span data-ttu-id="a42bd-194">0x800A0EA5</span><span class="sxs-lookup"><span data-stu-id="a42bd-194">0x800A0EA5</span></span></p></td>
<td><p><span data-ttu-id="a42bd-195">Error en la actualización de campos.</span><span class="sxs-lookup"><span data-stu-id="a42bd-195">Fields update failed.</span></span> <span data-ttu-id="a42bd-196">Para obtener más información, examine la propiedad <strong>Status</strong> de cada objeto de campo.</span><span class="sxs-lookup"><span data-stu-id="a42bd-196">For further information, examine the <strong>Status</strong> property of individual field objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-197"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-197"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-198">3219</span><span class="sxs-lookup"><span data-stu-id="a42bd-198">3219</span></span><br />
<span data-ttu-id="a42bd-199">-2146825069</span><span class="sxs-lookup"><span data-stu-id="a42bd-199">-2146825069</span></span><br />
<span data-ttu-id="a42bd-200">0x800A0C93</span><span class="sxs-lookup"><span data-stu-id="a42bd-200">0x800A0C93</span></span></p></td>
<td><p><span data-ttu-id="a42bd-201">Operación no permitida en este contexto.</span><span class="sxs-lookup"><span data-stu-id="a42bd-201">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-202"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-202"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-203">3719</span><span class="sxs-lookup"><span data-stu-id="a42bd-203">3719</span></span><br />
<span data-ttu-id="a42bd-204">-2146824569</span><span class="sxs-lookup"><span data-stu-id="a42bd-204">-2146824569</span></span><br />
<span data-ttu-id="a42bd-205">0x800A0E87</span><span class="sxs-lookup"><span data-stu-id="a42bd-205">0x800A0E87</span></span></p></td>
<td><p><span data-ttu-id="a42bd-206">El valor de los datos entra en conflicto con las restricciones de integridad del campo.</span><span class="sxs-lookup"><span data-stu-id="a42bd-206">Data value conflicts with the integrity constraints of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-207"><strong>adErrInTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-207"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-208">3246</span><span class="sxs-lookup"><span data-stu-id="a42bd-208">3246</span></span><br />
<span data-ttu-id="a42bd-209">-2146825042</span><span class="sxs-lookup"><span data-stu-id="a42bd-209">-2146825042</span></span><br />
<span data-ttu-id="a42bd-210">0x800A0CAE</span><span class="sxs-lookup"><span data-stu-id="a42bd-210">0x800A0CAE</span></span></p></td>
<td><p><span data-ttu-id="a42bd-211">No se puede cerrar explícitamente el objeto <strong>Connection</strong> mientras ocurre una transacción.</span><span class="sxs-lookup"><span data-stu-id="a42bd-211"><strong>Connection</strong> object cannot be explicitly closed while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-212"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-212"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-213">3001</span><span class="sxs-lookup"><span data-stu-id="a42bd-213">3001</span></span><br />
<span data-ttu-id="a42bd-214">-2146825287</span><span class="sxs-lookup"><span data-stu-id="a42bd-214">-2146825287</span></span><br />
<span data-ttu-id="a42bd-215">0x800A0BB9</span><span class="sxs-lookup"><span data-stu-id="a42bd-215">0x800A0BB9</span></span></p></td>
<td><p><span data-ttu-id="a42bd-216">Los argumentos no son del tipo correcto, están fuera del intervalo aceptable o en conflicto entre sí.</span><span class="sxs-lookup"><span data-stu-id="a42bd-216">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-217"><strong>adErrInvalidConnection</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-217"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-218">3709</span><span class="sxs-lookup"><span data-stu-id="a42bd-218">3709</span></span><br />
<span data-ttu-id="a42bd-219">-2146824579</span><span class="sxs-lookup"><span data-stu-id="a42bd-219">-2146824579</span></span><br />
<span data-ttu-id="a42bd-220">0x800A0E7D</span><span class="sxs-lookup"><span data-stu-id="a42bd-220">0x800A0E7D</span></span></p></td>
<td><p><span data-ttu-id="a42bd-221">No se puede utilizar la conexión para realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="a42bd-221">The connection cannot be used to perform this operation.</span></span> <span data-ttu-id="a42bd-222">Está cerrada o no es válida en este contexto.</span><span class="sxs-lookup"><span data-stu-id="a42bd-222">It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-223"><strong>adErrInvalidParamInfo</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-223"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-224">3708</span><span class="sxs-lookup"><span data-stu-id="a42bd-224">3708</span></span><br />
<span data-ttu-id="a42bd-225">-2146824580</span><span class="sxs-lookup"><span data-stu-id="a42bd-225">-2146824580</span></span><br />
<span data-ttu-id="a42bd-226">0x800A0E7C</span><span class="sxs-lookup"><span data-stu-id="a42bd-226">0x800A0E7C</span></span></p></td>
<td><p><span data-ttu-id="a42bd-227">El objeto <strong>Parameter</strong> no se ha definido correctamente.</span><span class="sxs-lookup"><span data-stu-id="a42bd-227"><strong>Parameter</strong> object is improperly defined.</span></span> <span data-ttu-id="a42bd-228">Se proporcionó información incoherente o incompleta.</span><span class="sxs-lookup"><span data-stu-id="a42bd-228">Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-229"><strong>adErrInvalidTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-229"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-230">3714</span><span class="sxs-lookup"><span data-stu-id="a42bd-230">3714</span></span><br />
<span data-ttu-id="a42bd-231">-2146824574</span><span class="sxs-lookup"><span data-stu-id="a42bd-231">-2146824574</span></span><br />
<span data-ttu-id="a42bd-232">0x800A0E82</span><span class="sxs-lookup"><span data-stu-id="a42bd-232">0x800A0E82</span></span></p></td>
<td><p><span data-ttu-id="a42bd-233">La transacción de coordinación no es válida o no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="a42bd-233">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-234"><strong>adErrInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-234"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-235">3729</span><span class="sxs-lookup"><span data-stu-id="a42bd-235">3729</span></span><br />
<span data-ttu-id="a42bd-236">-2146824559</span><span class="sxs-lookup"><span data-stu-id="a42bd-236">-2146824559</span></span><br />
<span data-ttu-id="a42bd-237">0x800A0E91</span><span class="sxs-lookup"><span data-stu-id="a42bd-237">0x800A0E91</span></span></p></td>
<td><p><span data-ttu-id="a42bd-238">La dirección URL contiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="a42bd-238">URL contains invalid characters.</span></span> <span data-ttu-id="a42bd-239">Asegúrese de que la dirección URL está escrita correctamente.</span><span class="sxs-lookup"><span data-stu-id="a42bd-239">Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-240"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-240"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-241">3265</span><span class="sxs-lookup"><span data-stu-id="a42bd-241">3265</span></span><br />
<span data-ttu-id="a42bd-242">-2146825023</span><span class="sxs-lookup"><span data-stu-id="a42bd-242">-2146825023</span></span><br />
<span data-ttu-id="a42bd-243">0x800A0CC1</span><span class="sxs-lookup"><span data-stu-id="a42bd-243">0x800A0CC1</span></span></p></td>
<td><p><span data-ttu-id="a42bd-244">No se puede encontrar el elemento en la colección correspondiente al ordinal o nombre solicitado.</span><span class="sxs-lookup"><span data-stu-id="a42bd-244">Item cannot be found in the collection corresponding to the requested name or ordinal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-245"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-245"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-246">3021</span><span class="sxs-lookup"><span data-stu-id="a42bd-246">3021</span></span><br />
<span data-ttu-id="a42bd-247">-2146825267</span><span class="sxs-lookup"><span data-stu-id="a42bd-247">-2146825267</span></span><br />
<span data-ttu-id="a42bd-248">0x800A0BCD</span><span class="sxs-lookup"><span data-stu-id="a42bd-248">0x800A0BCD</span></span></p></td>
<td><p><span data-ttu-id="a42bd-249"><strong>BOF</strong> o <strong>EOF</strong> es True, o bien el registro actual se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="a42bd-249">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted.</span></span> <span data-ttu-id="a42bd-250">La operación solicitada requiere un registro actual.</span><span class="sxs-lookup"><span data-stu-id="a42bd-250">Requested operation requires a current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-251"><strong>adErrNotExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-251"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-252">3715</span><span class="sxs-lookup"><span data-stu-id="a42bd-252">3715</span></span><br />
<span data-ttu-id="a42bd-253">-2146824573</span><span class="sxs-lookup"><span data-stu-id="a42bd-253">-2146824573</span></span><br />
<span data-ttu-id="a42bd-254">0x800A0E83</span><span class="sxs-lookup"><span data-stu-id="a42bd-254">0x800A0E83</span></span></p></td>
<td><p><span data-ttu-id="a42bd-255">No se puede realizar la operación mientras no se ejecute.</span><span class="sxs-lookup"><span data-stu-id="a42bd-255">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-256"><strong>adErrNotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-256"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-257">3710</span><span class="sxs-lookup"><span data-stu-id="a42bd-257">3710</span></span><br />
<span data-ttu-id="a42bd-258">-2146824578</span><span class="sxs-lookup"><span data-stu-id="a42bd-258">-2146824578</span></span><br />
<span data-ttu-id="a42bd-259">0x800A0E7E</span><span class="sxs-lookup"><span data-stu-id="a42bd-259">0x800A0E7E</span></span></p></td>
<td><p><span data-ttu-id="a42bd-260">No se puede realizar la operación mientras se procesa el evento.</span><span class="sxs-lookup"><span data-stu-id="a42bd-260">Operation cannot be performed while processing event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-261"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-261"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-262">3704</span><span class="sxs-lookup"><span data-stu-id="a42bd-262">3704</span></span><br />
<span data-ttu-id="a42bd-263">-2146824584</span><span class="sxs-lookup"><span data-stu-id="a42bd-263">-2146824584</span></span><br />
<span data-ttu-id="a42bd-264">0x800A0E78</span><span class="sxs-lookup"><span data-stu-id="a42bd-264">0x800A0E78</span></span></p></td>
<td><p><span data-ttu-id="a42bd-265">La operación no se permite cuando el objeto está cerrado.</span><span class="sxs-lookup"><span data-stu-id="a42bd-265">Operation is not allowed when the object is closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-266"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-266"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-267">3367</span><span class="sxs-lookup"><span data-stu-id="a42bd-267">3367</span></span><br />
<span data-ttu-id="a42bd-268">-2146824921</span><span class="sxs-lookup"><span data-stu-id="a42bd-268">-2146824921</span></span><br />
<span data-ttu-id="a42bd-269">0x800A0D27</span><span class="sxs-lookup"><span data-stu-id="a42bd-269">0x800A0D27</span></span></p></td>
<td><p><span data-ttu-id="a42bd-270">El objeto ya está en la colección.</span><span class="sxs-lookup"><span data-stu-id="a42bd-270">Object is already in collection.</span></span> <span data-ttu-id="a42bd-271">No se puede anexar.</span><span class="sxs-lookup"><span data-stu-id="a42bd-271">Cannot append.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-272"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-272"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-273">3420</span><span class="sxs-lookup"><span data-stu-id="a42bd-273">3420</span></span><br />
<span data-ttu-id="a42bd-274">-2146824868</span><span class="sxs-lookup"><span data-stu-id="a42bd-274">-2146824868</span></span><br />
<span data-ttu-id="a42bd-275">0x800A0D5C</span><span class="sxs-lookup"><span data-stu-id="a42bd-275">0x800A0D5C</span></span></p></td>
<td><p><span data-ttu-id="a42bd-276">El objeto ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="a42bd-276">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-277"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-277"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-278">3705</span><span class="sxs-lookup"><span data-stu-id="a42bd-278">3705</span></span><br />
<span data-ttu-id="a42bd-279">-2146824583</span><span class="sxs-lookup"><span data-stu-id="a42bd-279">-2146824583</span></span><br />
<span data-ttu-id="a42bd-280">0x800A0E79</span><span class="sxs-lookup"><span data-stu-id="a42bd-280">0x800A0E79</span></span></p></td>
<td><p><span data-ttu-id="a42bd-281">No se permite la operación cuando el objeto está abierto.</span><span class="sxs-lookup"><span data-stu-id="a42bd-281">Operation is not allowed when the object is open.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-282"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-282"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-283">3002</span><span class="sxs-lookup"><span data-stu-id="a42bd-283">3002</span></span><br />
<span data-ttu-id="a42bd-284">-2146825286</span><span class="sxs-lookup"><span data-stu-id="a42bd-284">-2146825286</span></span><br />
<span data-ttu-id="a42bd-285">0x800A0BBA</span><span class="sxs-lookup"><span data-stu-id="a42bd-285">0x800A0BBA</span></span></p></td>
<td><p><span data-ttu-id="a42bd-286">No se pudo abrir el archivo.</span><span class="sxs-lookup"><span data-stu-id="a42bd-286">File could not be opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-287"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-287"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-288">3712</span><span class="sxs-lookup"><span data-stu-id="a42bd-288">3712</span></span><br />
<span data-ttu-id="a42bd-289">-2146824576</span><span class="sxs-lookup"><span data-stu-id="a42bd-289">-2146824576</span></span><br />
<span data-ttu-id="a42bd-290">0x800A0E80</span><span class="sxs-lookup"><span data-stu-id="a42bd-290">0x800A0E80</span></span></p></td>
<td><p><span data-ttu-id="a42bd-291">La operación ha sido cancelada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="a42bd-291">Operation has been cancelled by the user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-292"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-292"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-293">3734</span><span class="sxs-lookup"><span data-stu-id="a42bd-293">3734</span></span><br />
<span data-ttu-id="a42bd-294">-2146824554</span><span class="sxs-lookup"><span data-stu-id="a42bd-294">-2146824554</span></span><br />
<span data-ttu-id="a42bd-295">0x800A0E96</span><span class="sxs-lookup"><span data-stu-id="a42bd-295">0x800A0E96</span></span></p></td>
<td><p><span data-ttu-id="a42bd-296">No se puede realizar operación.</span><span class="sxs-lookup"><span data-stu-id="a42bd-296">Operation cannot be performed.</span></span> <span data-ttu-id="a42bd-297">El proveedor no puede obtener suficiente espacio de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="a42bd-297">Provider cannot obtain enough storage space.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-298"><strong>adErrPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-298"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-299">3720</span><span class="sxs-lookup"><span data-stu-id="a42bd-299">3720</span></span><br />
<span data-ttu-id="a42bd-300">-2146824568</span><span class="sxs-lookup"><span data-stu-id="a42bd-300">-2146824568</span></span><br />
<span data-ttu-id="a42bd-301">0x800A0E88</span><span class="sxs-lookup"><span data-stu-id="a42bd-301">0x800A0E88</span></span></p></td>
<td><p><span data-ttu-id="a42bd-302">La falta de permiso suficiente impide escribir en el campo.</span><span class="sxs-lookup"><span data-stu-id="a42bd-302">Insufficent permission prevents writing to the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-303"><strong>adErrProviderFailed</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-303"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-304">3000</span><span class="sxs-lookup"><span data-stu-id="a42bd-304">3000</span></span><br />
<span data-ttu-id="a42bd-305">-2146825288</span><span class="sxs-lookup"><span data-stu-id="a42bd-305">-2146825288</span></span><br />
<span data-ttu-id="a42bd-306">0x800A0BB8</span><span class="sxs-lookup"><span data-stu-id="a42bd-306">0x800A0BB8</span></span></p></td>
<td><p><span data-ttu-id="a42bd-307">El proveedor no pudo realizar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="a42bd-307">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-308"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-308"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-309">3706</span><span class="sxs-lookup"><span data-stu-id="a42bd-309">3706</span></span><br />
<span data-ttu-id="a42bd-310">-2146824582</span><span class="sxs-lookup"><span data-stu-id="a42bd-310">-2146824582</span></span><br />
<span data-ttu-id="a42bd-311">0x800A0E7A</span><span class="sxs-lookup"><span data-stu-id="a42bd-311">0x800A0E7A</span></span></p></td>
<td><p><span data-ttu-id="a42bd-p113">No se puede encontrar un proveedor.Es posible que no se haya instalado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a42bd-p113">Provider cannot be found. It may not be properly installed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-314"><strong>adErrReadFile</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-314"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-315">3003</span><span class="sxs-lookup"><span data-stu-id="a42bd-315">3003</span></span><br />
<span data-ttu-id="a42bd-316">-2146825285</span><span class="sxs-lookup"><span data-stu-id="a42bd-316">-2146825285</span></span><br />
<span data-ttu-id="a42bd-317">0x800A0BBB</span><span class="sxs-lookup"><span data-stu-id="a42bd-317">0x800A0BBB</span></span></p></td>
<td><p><span data-ttu-id="a42bd-318">No se pudo leer el archivo.</span><span class="sxs-lookup"><span data-stu-id="a42bd-318">File could not be read.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-319"><strong>adErrResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-319"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-320">3731</span><span class="sxs-lookup"><span data-stu-id="a42bd-320">3731</span></span><br />
<span data-ttu-id="a42bd-321">-2146824557</span><span class="sxs-lookup"><span data-stu-id="a42bd-321">-2146824557</span></span><br />
<span data-ttu-id="a42bd-322">0x800A0E93</span><span class="sxs-lookup"><span data-stu-id="a42bd-322">0x800A0E93</span></span></p></td>
<td><p><span data-ttu-id="a42bd-323">No se puede realizar una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="a42bd-323">Copy operation cannot be performed.</span></span> <span data-ttu-id="a42bd-324">El objeto mencionado en la dirección URL de destino ya existe.</span><span class="sxs-lookup"><span data-stu-id="a42bd-324">Object named by destination URL already exists.</span></span> <span data-ttu-id="a42bd-325">Especifique <strong>adCopyOverwrite</strong> para reemplazar el objeto.</span><span class="sxs-lookup"><span data-stu-id="a42bd-325">Specify <strong>adCopyOverwrite</strong> to replace the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-326"><strong>adErrResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-326"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-327">3730</span><span class="sxs-lookup"><span data-stu-id="a42bd-327">3730</span></span><br />
<span data-ttu-id="a42bd-328">-2146824558</span><span class="sxs-lookup"><span data-stu-id="a42bd-328">-2146824558</span></span><br />
<span data-ttu-id="a42bd-329">0x800A0E92</span><span class="sxs-lookup"><span data-stu-id="a42bd-329">0x800A0E92</span></span></p></td>
<td><p><span data-ttu-id="a42bd-p115">Un objeto representado por la dirección URL especificada está bloqueado por uno o más procesos. Espere hasta que el proceso haya finalizado e intente de nuevo la operación.</span><span class="sxs-lookup"><span data-stu-id="a42bd-p115">Object represented by the specified URL is locked by one or more other processes. Wait until the process has finished and attempt the operation again.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-332"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-332"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-333">3735</span><span class="sxs-lookup"><span data-stu-id="a42bd-333">3735</span></span><br />
<span data-ttu-id="a42bd-334">-2146824553</span><span class="sxs-lookup"><span data-stu-id="a42bd-334">-2146824553</span></span><br />
<span data-ttu-id="a42bd-335">0x800A0E97</span><span class="sxs-lookup"><span data-stu-id="a42bd-335">0x800A0E97</span></span></p></td>
<td><p><span data-ttu-id="a42bd-336">La dirección URL de origen o destino está fuera del ámbito del registro actual.</span><span class="sxs-lookup"><span data-stu-id="a42bd-336">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-337"><strong>adErrSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-337"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-338">3722</span><span class="sxs-lookup"><span data-stu-id="a42bd-338">3722</span></span><br />
<span data-ttu-id="a42bd-339">-2146824566</span><span class="sxs-lookup"><span data-stu-id="a42bd-339">-2146824566</span></span><br />
<span data-ttu-id="a42bd-340">0x800A0E8A</span><span class="sxs-lookup"><span data-stu-id="a42bd-340">0x800A0E8A</span></span></p></td>
<td><p><span data-ttu-id="a42bd-341">El valor de los datos entra en conflicto con el tipo de datos o las restricciones del campo.</span><span class="sxs-lookup"><span data-stu-id="a42bd-341">Data value conflicts with the data type or constraints of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-342"><strong>adErrSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-342"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-343">3723</span><span class="sxs-lookup"><span data-stu-id="a42bd-343">3723</span></span><br />
<span data-ttu-id="a42bd-344">-2146824565</span><span class="sxs-lookup"><span data-stu-id="a42bd-344">-2146824565</span></span><br />
<span data-ttu-id="a42bd-345">0x800A0E8B</span><span class="sxs-lookup"><span data-stu-id="a42bd-345">0x800A0E8B</span></span></p></td>
<td><p><span data-ttu-id="a42bd-346">La conversión produjo un error porque el valor de los datos tenía signo y el tipo de datos de campo utilizado por el proveedor no tenía signo.</span><span class="sxs-lookup"><span data-stu-id="a42bd-346">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-347"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-347"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-348">3713</span><span class="sxs-lookup"><span data-stu-id="a42bd-348">3713</span></span><br />
<span data-ttu-id="a42bd-349">-2146824575</span><span class="sxs-lookup"><span data-stu-id="a42bd-349">-2146824575</span></span><br />
<span data-ttu-id="a42bd-350">0x800A0E81</span><span class="sxs-lookup"><span data-stu-id="a42bd-350">0x800A0E81</span></span></p></td>
<td><p><span data-ttu-id="a42bd-351">No se puede realizar la operación mientras se conecta asincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="a42bd-351">Operation cannot be performed while connecting aynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-352"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-352"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-353">3711</span><span class="sxs-lookup"><span data-stu-id="a42bd-353">3711</span></span><br />
<span data-ttu-id="a42bd-354">-2146824577</span><span class="sxs-lookup"><span data-stu-id="a42bd-354">-2146824577</span></span><br />
<span data-ttu-id="a42bd-355">0x800A0E7F</span><span class="sxs-lookup"><span data-stu-id="a42bd-355">0x800A0E7F</span></span></p></td>
<td><p><span data-ttu-id="a42bd-356">No se puede realizar la operación mientras se ejecuta asincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="a42bd-356">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-357"><strong>adErrTreePermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-357"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-358">3728</span><span class="sxs-lookup"><span data-stu-id="a42bd-358">3728</span></span><br />
<span data-ttu-id="a42bd-359">-2146824560</span><span class="sxs-lookup"><span data-stu-id="a42bd-359">-2146824560</span></span><br />
<span data-ttu-id="a42bd-360">0x800A0E90</span><span class="sxs-lookup"><span data-stu-id="a42bd-360">0x800A0E90</span></span></p></td>
<td><p><span data-ttu-id="a42bd-361">Los permisos son insuficientes para tener acceso a un árbol o subárbol.</span><span class="sxs-lookup"><span data-stu-id="a42bd-361">Permissions are insufficient to access tree or subtree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-362"><strong>adErrUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-362"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-363">3736</span><span class="sxs-lookup"><span data-stu-id="a42bd-363">3736</span></span><br />
<span data-ttu-id="a42bd-364">-2146824552</span><span class="sxs-lookup"><span data-stu-id="a42bd-364">-2146824552</span></span><br />
<span data-ttu-id="a42bd-365">0x800A0E98</span><span class="sxs-lookup"><span data-stu-id="a42bd-365">0x800A0E98</span></span></p></td>
<td><p><span data-ttu-id="a42bd-366">La operación no se pudo completar y el estado no está disponible.</span><span class="sxs-lookup"><span data-stu-id="a42bd-366">Operation failed to complete and the status is unavailable.</span></span> <span data-ttu-id="a42bd-367">El campo puede no estar disponible o no se intentó la operación.</span><span class="sxs-lookup"><span data-stu-id="a42bd-367">The field may be unavailable or the operation was not attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-368"><strong>adErrUnsafeOperation</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-368"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-369">3716</span><span class="sxs-lookup"><span data-stu-id="a42bd-369">3716</span></span><br />
<span data-ttu-id="a42bd-370">-2146824572</span><span class="sxs-lookup"><span data-stu-id="a42bd-370">-2146824572</span></span><br />
<span data-ttu-id="a42bd-371">0x800A0E84</span><span class="sxs-lookup"><span data-stu-id="a42bd-371">0x800A0E84</span></span></p></td>
<td><p><span data-ttu-id="a42bd-372">La configuración de seguridad de este equipo prohíbe tener acceso a un origen de datos en otro dominio.</span><span class="sxs-lookup"><span data-stu-id="a42bd-372">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-373"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-373"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-374">3727</span><span class="sxs-lookup"><span data-stu-id="a42bd-374">3727</span></span><br />
<span data-ttu-id="a42bd-375">-2146824561</span><span class="sxs-lookup"><span data-stu-id="a42bd-375">-2146824561</span></span><br />
<span data-ttu-id="a42bd-376">0x800A0E8F</span><span class="sxs-lookup"><span data-stu-id="a42bd-376">0x800A0E8F</span></span></p></td>
<td><p><span data-ttu-id="a42bd-377">No existe la dirección URL de origen o el elemento principal de la dirección URL de destino.</span><span class="sxs-lookup"><span data-stu-id="a42bd-377">Either the source URL or the parent of the destination URL does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-378"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-378"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-379">3737</span><span class="sxs-lookup"><span data-stu-id="a42bd-379">3737</span></span><br />
<span data-ttu-id="a42bd-380">-2146824551</span><span class="sxs-lookup"><span data-stu-id="a42bd-380">-2146824551</span></span><br />
<span data-ttu-id="a42bd-381">0x800A0E99</span><span class="sxs-lookup"><span data-stu-id="a42bd-381">0x800A0E99</span></span></p></td>
<td><p><span data-ttu-id="a42bd-382">El registro al que ha asignado un nombre esta dirección URL no existe.</span><span class="sxs-lookup"><span data-stu-id="a42bd-382">Record named by this URL does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-383"><strong>adErrVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-383"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-384">3733</span><span class="sxs-lookup"><span data-stu-id="a42bd-384">3733</span></span><br />
<span data-ttu-id="a42bd-385">-2146824555</span><span class="sxs-lookup"><span data-stu-id="a42bd-385">-2146824555</span></span><br />
<span data-ttu-id="a42bd-386">0x800A0E95</span><span class="sxs-lookup"><span data-stu-id="a42bd-386">0x800A0E95</span></span></p></td>
<td><p><span data-ttu-id="a42bd-387">El proveedor no puede encontrar el dispositivo de almacenamiento que indica la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="a42bd-387">Provider cannot locate the storage device indicated by the URL.</span></span> <span data-ttu-id="a42bd-388">Asegúrese de que la dirección URL está escrita correctamente.</span><span class="sxs-lookup"><span data-stu-id="a42bd-388">Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-389"><strong>adErrWriteFile</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-389"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-390">3004</span><span class="sxs-lookup"><span data-stu-id="a42bd-390">3004</span></span><br />
<span data-ttu-id="a42bd-391">-2146825284</span><span class="sxs-lookup"><span data-stu-id="a42bd-391">-2146825284</span></span><br />
<span data-ttu-id="a42bd-392">0x800A0BBC</span><span class="sxs-lookup"><span data-stu-id="a42bd-392">0x800A0BBC</span></span></p></td>
<td><p><span data-ttu-id="a42bd-393">Error en la escritura en un archivo.</span><span class="sxs-lookup"><span data-stu-id="a42bd-393">Write to file failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-394"><strong>adWrnSecurityDialog</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-394"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-395">3717</span><span class="sxs-lookup"><span data-stu-id="a42bd-395">3717</span></span><br />
<span data-ttu-id="a42bd-396">-2146824571</span><span class="sxs-lookup"><span data-stu-id="a42bd-396">-2146824571</span></span><br />
<span data-ttu-id="a42bd-397">0x800A0E85</span><span class="sxs-lookup"><span data-stu-id="a42bd-397">0x800A0E85</span></span></p></td>
<td><p><span data-ttu-id="a42bd-398">Sólo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="a42bd-398">For internal use only.</span></span> <span data-ttu-id="a42bd-399">No la utilice.</span><span class="sxs-lookup"><span data-stu-id="a42bd-399">Don't use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-400"><strong>adWrnSecurityDialogHeader</strong></span><span class="sxs-lookup"><span data-stu-id="a42bd-400"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="a42bd-401">3718</span><span class="sxs-lookup"><span data-stu-id="a42bd-401">3718</span></span><br />
<span data-ttu-id="a42bd-402">-2146824570</span><span class="sxs-lookup"><span data-stu-id="a42bd-402">-2146824570</span></span><br />
<span data-ttu-id="a42bd-403">0x800A0E86</span><span class="sxs-lookup"><span data-stu-id="a42bd-403">0x800A0E86</span></span></p></td>
<td><p><span data-ttu-id="a42bd-404">Sólo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="a42bd-404">For internal use only.</span></span> <span data-ttu-id="a42bd-405">No la utilice.</span><span class="sxs-lookup"><span data-stu-id="a42bd-405">Don't use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="a42bd-406">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="a42bd-406">ADO/WFC equivalent</span></span>

<span data-ttu-id="a42bd-407">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="a42bd-407">Package: **com.ms.wfc.data**</span></span>

<span data-ttu-id="a42bd-408">Se definen sólo los subconjuntos siguientes de equivalentes ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="a42bd-408">Only the following subsets of ADO/WFC equivalents are defined.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a42bd-409">Constante</span><span class="sxs-lookup"><span data-stu-id="a42bd-409">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-410">AdoEnums. Valordeerror. BOUNDTOCOMMAND</span><span class="sxs-lookup"><span data-stu-id="a42bd-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-411">AdoEnums. Valordeerror. conVERSION</span><span class="sxs-lookup"><span data-stu-id="a42bd-411">AdoEnums.ErrorValue.DATACONVERSION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-412">AdoEnums. Valordeerror. FEATURENOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="a42bd-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-413">AdoEnums. Valordeerror. ILLEGALOPERATION</span><span class="sxs-lookup"><span data-stu-id="a42bd-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-414">AdoEnums. Valordeerror. inTRANSACTION</span><span class="sxs-lookup"><span data-stu-id="a42bd-414">AdoEnums.ErrorValue.INTRANSACTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-415">AdoEnums. Valordeerror. INVALIDARGUMENT</span><span class="sxs-lookup"><span data-stu-id="a42bd-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-416">AdoEnums. Valordeerror. INVALIDCONNECTION</span><span class="sxs-lookup"><span data-stu-id="a42bd-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-417">AdoEnums. Valordeerror. INVALIDPARAMINFO</span><span class="sxs-lookup"><span data-stu-id="a42bd-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-418">AdoEnums. Valordeerror. ITEMNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="a42bd-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-419">AdoEnums. Valordeerror. NOCURRENTRECORD</span><span class="sxs-lookup"><span data-stu-id="a42bd-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-420">AdoEnums. Valordeerror. NOTEXECUTING</span><span class="sxs-lookup"><span data-stu-id="a42bd-420">AdoEnums.ErrorValue.NOTEXECUTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-421">AdoEnums. Valordeerror. NOTREENTRANT</span><span class="sxs-lookup"><span data-stu-id="a42bd-421">AdoEnums.ErrorValue.NOTREENTRANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-422">AdoEnums. Valordeerror. OBJECTCLOSED</span><span class="sxs-lookup"><span data-stu-id="a42bd-422">AdoEnums.ErrorValue.OBJECTCLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-423">AdoEnums. Valordeerror. OBJECTINCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="a42bd-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-424">AdoEnums. Valordeerror. OBJECTNOTSET</span><span class="sxs-lookup"><span data-stu-id="a42bd-424">AdoEnums.ErrorValue.OBJECTNOTSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-425">AdoEnums. Valordeerror. OPENOBJETO</span><span class="sxs-lookup"><span data-stu-id="a42bd-425">AdoEnums.ErrorValue.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-426">AdoEnums. Valordeerror. OPERATIONCANCELLED</span><span class="sxs-lookup"><span data-stu-id="a42bd-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-427">AdoEnums. Valordeerror. PROVIDERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="a42bd-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-428">AdoEnums. Valordeerror. STILLCONNECTING</span><span class="sxs-lookup"><span data-stu-id="a42bd-428">AdoEnums.ErrorValue.STILLCONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a42bd-429">AdoEnums. Valordeerror. STILLEXECUTING</span><span class="sxs-lookup"><span data-stu-id="a42bd-429">AdoEnums.ErrorValue.STILLEXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a42bd-430">AdoEnums. Valordeerror. UNSAFEOPERATION</span><span class="sxs-lookup"><span data-stu-id="a42bd-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span></span></p></td>
</tr>
</tbody>
</table>

