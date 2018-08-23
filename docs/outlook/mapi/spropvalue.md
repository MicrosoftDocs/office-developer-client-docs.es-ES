---
title: SPropValue
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropValue
api_type:
- COM
ms.assetid: faf795a2-84db-432d-a05f-082f25a5cab5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 60528162917a8a383060adbcadefb610aa42ce32
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580974"
---
# <a name="spropvalue"></a><span data-ttu-id="7d3ac-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7d3ac-103">SPropValue</span></span>

  
  
<span data-ttu-id="7d3ac-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d3ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d3ac-105">Describe una propiedad MAPI.</span><span class="sxs-lookup"><span data-stu-id="7d3ac-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7d3ac-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7d3ac-106">Header file:</span></span>  <br/> |<span data-ttu-id="7d3ac-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7d3ac-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7d3ac-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="7d3ac-108">Related macros:</span></span>  <br/> |<span data-ttu-id="7d3ac-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="7d3ac-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="7d3ac-110">Members</span><span class="sxs-lookup"><span data-stu-id="7d3ac-110">Members</span></span>

 <span data-ttu-id="7d3ac-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="7d3ac-112">Etiqueta de la propiedad para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="7d3ac-112">Property tag for the property.</span></span> <span data-ttu-id="7d3ac-113">Las etiquetas de propiedad son enteros sin signo de 32 bits que consta del identificador único de la propiedad de orden superior a 16 bits y el tipo de propiedad de orden inferior a 16 bits.</span><span class="sxs-lookup"><span data-stu-id="7d3ac-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="7d3ac-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="7d3ac-115">Reservado para MAPI; No use.</span><span class="sxs-lookup"><span data-stu-id="7d3ac-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="7d3ac-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-116">**Value**</span></span>
  
> <span data-ttu-id="7d3ac-117">Unión de los valores de datos, el valor específico determinado por el tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="7d3ac-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="7d3ac-118">En la siguiente tabla se enumera para cada tipo de propiedad, el miembro de la unión que se debe usar y su tipo de datos asociado.</span><span class="sxs-lookup"><span data-stu-id="7d3ac-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="7d3ac-119">**Tipo de propiedad**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-119">**Property type**</span></span>|<span data-ttu-id="7d3ac-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-120">**Value**</span></span>|<span data-ttu-id="7d3ac-121">**Tipo de datos del valor**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7d3ac-122">PT_I2 o PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="7d3ac-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="7d3ac-123">**i**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-123">**i**</span></span> <br/> |<span data-ttu-id="7d3ac-124">short int</span><span class="sxs-lookup"><span data-stu-id="7d3ac-124">short int</span></span>  <br/> |
|<span data-ttu-id="7d3ac-125">PT_I4 o PT_LONG (firmado)</span><span class="sxs-lookup"><span data-stu-id="7d3ac-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="7d3ac-126">**l**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-126">**l**</span></span> <br/> |<span data-ttu-id="7d3ac-127">LARGO</span><span class="sxs-lookup"><span data-stu-id="7d3ac-127">LONG</span></span>  <br/> |
|<span data-ttu-id="7d3ac-128">PT_I4 o PT_LONG (sin firmar)</span><span class="sxs-lookup"><span data-stu-id="7d3ac-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="7d3ac-129">**UL**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-129">**ul**</span></span> <br/> |<span data-ttu-id="7d3ac-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="7d3ac-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="7d3ac-131">PT_R4 o PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="7d3ac-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="7d3ac-132">**flt**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-132">**flt**</span></span> <br/> |<span data-ttu-id="7d3ac-133">float</span><span class="sxs-lookup"><span data-stu-id="7d3ac-133">float</span></span>  <br/> |
|<span data-ttu-id="7d3ac-134">PT_R8 o PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="7d3ac-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="7d3ac-135">**doble**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-135">**dbl**</span></span> <br/> |<span data-ttu-id="7d3ac-136">double</span><span class="sxs-lookup"><span data-stu-id="7d3ac-136">double</span></span>  <br/> |
|<span data-ttu-id="7d3ac-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7d3ac-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="7d3ac-138">**b**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-138">**b**</span></span> <br/> |<span data-ttu-id="7d3ac-139">int corto sin firmar</span><span class="sxs-lookup"><span data-stu-id="7d3ac-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="7d3ac-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="7d3ac-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="7d3ac-141">**actual**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-141">**cur**</span></span> <br/> |[<span data-ttu-id="7d3ac-142">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="7d3ac-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="7d3ac-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="7d3ac-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="7d3ac-144">**en**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-144">**at**</span></span> <br/> |<span data-ttu-id="7d3ac-145">double</span><span class="sxs-lookup"><span data-stu-id="7d3ac-145">double</span></span>  <br/> |
|<span data-ttu-id="7d3ac-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="7d3ac-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="7d3ac-147">**FT**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-147">**ft**</span></span> <br/> |[<span data-ttu-id="7d3ac-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="7d3ac-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="7d3ac-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="7d3ac-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="7d3ac-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-150">**lpszA**</span></span> <br/> |<span data-ttu-id="7d3ac-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="7d3ac-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="7d3ac-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7d3ac-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="7d3ac-153">**Papelera de**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-153">**bin**</span></span> <br/> |<span data-ttu-id="7d3ac-154">BYTE [matriz]</span><span class="sxs-lookup"><span data-stu-id="7d3ac-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="7d3ac-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7d3ac-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="7d3ac-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-156">**lpszW**</span></span> <br/> |<span data-ttu-id="7d3ac-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="7d3ac-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="7d3ac-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="7d3ac-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="7d3ac-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-159">**lpguid**</span></span> <br/> |<span data-ttu-id="7d3ac-160">LPGUID</span><span class="sxs-lookup"><span data-stu-id="7d3ac-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="7d3ac-161">PT_I8 o PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="7d3ac-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="7d3ac-162">**li**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-162">**li**</span></span> <br/> |<span data-ttu-id="7d3ac-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="7d3ac-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="7d3ac-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="7d3ac-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-165">**MVi**</span></span> <br/> |[<span data-ttu-id="7d3ac-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="7d3ac-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="7d3ac-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="7d3ac-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="7d3ac-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-168">**MVI**</span></span> <br/> |[<span data-ttu-id="7d3ac-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="7d3ac-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="7d3ac-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="7d3ac-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="7d3ac-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="7d3ac-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="7d3ac-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="7d3ac-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="7d3ac-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="7d3ac-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="7d3ac-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="7d3ac-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="7d3ac-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="7d3ac-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="7d3ac-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="7d3ac-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="7d3ac-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="7d3ac-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="7d3ac-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="7d3ac-180">**MVat**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-180">**MVat**</span></span> <br/> |[<span data-ttu-id="7d3ac-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="7d3ac-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="7d3ac-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="7d3ac-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="7d3ac-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-183">**MVft**</span></span> <br/> |[<span data-ttu-id="7d3ac-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="7d3ac-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="7d3ac-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="7d3ac-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="7d3ac-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="7d3ac-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="7d3ac-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="7d3ac-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="7d3ac-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="7d3ac-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="7d3ac-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="7d3ac-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="7d3ac-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7d3ac-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="7d3ac-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="7d3ac-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="7d3ac-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="7d3ac-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="7d3ac-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="7d3ac-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="7d3ac-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="7d3ac-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="7d3ac-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="7d3ac-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="7d3ac-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-198">**MVli**</span></span> <br/> |[<span data-ttu-id="7d3ac-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="7d3ac-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="7d3ac-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="7d3ac-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="7d3ac-201">**err**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-201">**err**</span></span> <br/> |[<span data-ttu-id="7d3ac-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="7d3ac-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="7d3ac-203">PT_NULL o pt Object</span><span class="sxs-lookup"><span data-stu-id="7d3ac-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="7d3ac-204">**x**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-204">**x**</span></span> <br/> |<span data-ttu-id="7d3ac-205">LARGO</span><span class="sxs-lookup"><span data-stu-id="7d3ac-205">LONG</span></span>  <br/> |
|<span data-ttu-id="7d3ac-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="7d3ac-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="7d3ac-207">**LPV**</span><span class="sxs-lookup"><span data-stu-id="7d3ac-207">**lpv**</span></span> <br/> |<span data-ttu-id="7d3ac-208">VOID\*</span><span class="sxs-lookup"><span data-stu-id="7d3ac-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d3ac-209">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7d3ac-209">Remarks</span></span>

<span data-ttu-id="7d3ac-210">El miembro **ulPropTag** se compone de dos partes:</span><span class="sxs-lookup"><span data-stu-id="7d3ac-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="7d3ac-211">Un identificador de orden superior a 16 bits.</span><span class="sxs-lookup"><span data-stu-id="7d3ac-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="7d3ac-212">Un tipo de orden inferior a 16 bits.</span><span class="sxs-lookup"><span data-stu-id="7d3ac-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="7d3ac-213">El identificador es un valor numérico dentro de un intervalo determinado.</span><span class="sxs-lookup"><span data-stu-id="7d3ac-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="7d3ac-214">MAPI define los intervalos para los identificadores describir la propiedad que se usa para y quién es responsable de mantenerlo.</span><span class="sxs-lookup"><span data-stu-id="7d3ac-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="7d3ac-215">MAPI define restricciones para cada una de las etiquetas de propiedad que admite en el archivo de encabezado Mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="7d3ac-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="7d3ac-216">El tipo indica el formato para el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="7d3ac-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="7d3ac-217">MAPI define constantes para cada uno de los tipos de propiedad que admite en el archivo de encabezado Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="7d3ac-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="7d3ac-218">Para obtener una lista completa de los intervalos de propiedad válido para los identificadores y tipos de propiedad, consulte el apéndice [identificadores de propiedades y tipos](property-identifiers-and-types.md) .</span><span class="sxs-lookup"><span data-stu-id="7d3ac-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="7d3ac-219">El miembro **dwAlignPad** se utiliza como relleno para realizar la alineación adecuada seguro en los equipos que requieren la alineación de 8 bytes para los valores de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="7d3ac-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="7d3ac-220">Los desarrolladores que escribir código en estos equipos deben utilizar rutinas de asignación de memoria que asignan las matrices **SPropValue** en límites de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="7d3ac-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="7d3ac-221">Para obtener más información, vea [Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md) y [Actualizar las propiedades de MAPI](updating-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="7d3ac-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7d3ac-222">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="7d3ac-222">See also</span></span>



[<span data-ttu-id="7d3ac-223">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="7d3ac-223">MAPI Structures</span></span>](mapi-structures.md)

