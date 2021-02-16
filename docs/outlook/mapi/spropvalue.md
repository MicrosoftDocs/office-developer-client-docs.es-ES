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
ms.openlocfilehash: c7f4e8835831af6277cef134bf3961e9928cba33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433531"
---
# <a name="spropvalue"></a><span data-ttu-id="5f1e2-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="5f1e2-103">SPropValue</span></span>

  
  
<span data-ttu-id="5f1e2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f1e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f1e2-105">Describe una propiedad MAPI.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f1e2-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="5f1e2-106">Header file:</span></span>  <br/> |<span data-ttu-id="5f1e2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f1e2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5f1e2-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="5f1e2-108">Related macros:</span></span>  <br/> |<span data-ttu-id="5f1e2-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="5f1e2-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="5f1e2-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="5f1e2-110">Members</span></span>

 <span data-ttu-id="5f1e2-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="5f1e2-112">Etiqueta de propiedad de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-112">Property tag for the property.</span></span> <span data-ttu-id="5f1e2-113">Las etiquetas de propiedad son enteros sin signo de 32 bits formados por el identificador único de la propiedad en el orden alto de 16 bits y el tipo de la propiedad en orden bajo de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="5f1e2-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="5f1e2-115">Reservado para MAPI; no usar.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="5f1e2-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-116">**Value**</span></span>
  
> <span data-ttu-id="5f1e2-117">Unión de valores de datos, el valor específico determinado por el tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="5f1e2-118">En la tabla siguiente se enumeran cada tipo de propiedad, el miembro de la unión que se debe usar y su tipo de datos asociado.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="5f1e2-119">**Tipo de propiedad**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-119">**Property type**</span></span>|<span data-ttu-id="5f1e2-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-120">**Value**</span></span>|<span data-ttu-id="5f1e2-121">**Tipo de datos del valor**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5f1e2-122">PT_I2 o PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="5f1e2-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="5f1e2-123">**i**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-123">**i**</span></span> <br/> |<span data-ttu-id="5f1e2-124">short int</span><span class="sxs-lookup"><span data-stu-id="5f1e2-124">short int</span></span>  <br/> |
|<span data-ttu-id="5f1e2-125">PT_I4 o PT_LONG (firmado)</span><span class="sxs-lookup"><span data-stu-id="5f1e2-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="5f1e2-126">**l**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-126">**l**</span></span> <br/> |<span data-ttu-id="5f1e2-127">LONG</span><span class="sxs-lookup"><span data-stu-id="5f1e2-127">LONG</span></span>  <br/> |
|<span data-ttu-id="5f1e2-128">PT_I4 o PT_LONG (sin signo)</span><span class="sxs-lookup"><span data-stu-id="5f1e2-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="5f1e2-129">**ul**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-129">**ul**</span></span> <br/> |<span data-ttu-id="5f1e2-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="5f1e2-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="5f1e2-131">PT_R4 o PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="5f1e2-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="5f1e2-132">**flt**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-132">**flt**</span></span> <br/> |<span data-ttu-id="5f1e2-133">float</span><span class="sxs-lookup"><span data-stu-id="5f1e2-133">float</span></span>  <br/> |
|<span data-ttu-id="5f1e2-134">PT_R8 o PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="5f1e2-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="5f1e2-135">**dbl**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-135">**dbl**</span></span> <br/> |<span data-ttu-id="5f1e2-136">double</span><span class="sxs-lookup"><span data-stu-id="5f1e2-136">double</span></span>  <br/> |
|<span data-ttu-id="5f1e2-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5f1e2-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="5f1e2-138">**b**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-138">**b**</span></span> <br/> |<span data-ttu-id="5f1e2-139">unsigned short int</span><span class="sxs-lookup"><span data-stu-id="5f1e2-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="5f1e2-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="5f1e2-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="5f1e2-141">**cur**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-141">**cur**</span></span> <br/> |[<span data-ttu-id="5f1e2-142">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="5f1e2-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="5f1e2-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="5f1e2-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="5f1e2-144">**at**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-144">**at**</span></span> <br/> |<span data-ttu-id="5f1e2-145">double</span><span class="sxs-lookup"><span data-stu-id="5f1e2-145">double</span></span>  <br/> |
|<span data-ttu-id="5f1e2-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5f1e2-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="5f1e2-147">**ft**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-147">**ft**</span></span> <br/> |[<span data-ttu-id="5f1e2-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="5f1e2-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="5f1e2-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="5f1e2-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="5f1e2-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-150">**lpszA**</span></span> <br/> |<span data-ttu-id="5f1e2-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="5f1e2-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="5f1e2-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5f1e2-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="5f1e2-153">**bin**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-153">**bin**</span></span> <br/> |<span data-ttu-id="5f1e2-154">BYTE [matriz]</span><span class="sxs-lookup"><span data-stu-id="5f1e2-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="5f1e2-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5f1e2-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="5f1e2-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-156">**lpszW**</span></span> <br/> |<span data-ttu-id="5f1e2-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5f1e2-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="5f1e2-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="5f1e2-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="5f1e2-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-159">**lpguid**</span></span> <br/> |<span data-ttu-id="5f1e2-160">LPGUID</span><span class="sxs-lookup"><span data-stu-id="5f1e2-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="5f1e2-161">PT_I8 o PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="5f1e2-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="5f1e2-162">**li**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-162">**li**</span></span> <br/> |<span data-ttu-id="5f1e2-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="5f1e2-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="5f1e2-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="5f1e2-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-165">**MVi**</span></span> <br/> |[<span data-ttu-id="5f1e2-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="5f1e2-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="5f1e2-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="5f1e2-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="5f1e2-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-168">**MVI**</span></span> <br/> |[<span data-ttu-id="5f1e2-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="5f1e2-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="5f1e2-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="5f1e2-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="5f1e2-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="5f1e2-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="5f1e2-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="5f1e2-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="5f1e2-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="5f1e2-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="5f1e2-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="5f1e2-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="5f1e2-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="5f1e2-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="5f1e2-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="5f1e2-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="5f1e2-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="5f1e2-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="5f1e2-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="5f1e2-180">**MVat**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-180">**MVat**</span></span> <br/> |[<span data-ttu-id="5f1e2-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="5f1e2-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="5f1e2-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5f1e2-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="5f1e2-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-183">**MVft**</span></span> <br/> |[<span data-ttu-id="5f1e2-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="5f1e2-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="5f1e2-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="5f1e2-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="5f1e2-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="5f1e2-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="5f1e2-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="5f1e2-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="5f1e2-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="5f1e2-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="5f1e2-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="5f1e2-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="5f1e2-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5f1e2-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="5f1e2-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="5f1e2-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="5f1e2-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="5f1e2-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="5f1e2-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="5f1e2-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="5f1e2-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="5f1e2-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="5f1e2-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="5f1e2-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="5f1e2-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-198">**MVli**</span></span> <br/> |[<span data-ttu-id="5f1e2-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="5f1e2-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="5f1e2-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="5f1e2-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="5f1e2-201">**err**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-201">**err**</span></span> <br/> |[<span data-ttu-id="5f1e2-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="5f1e2-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="5f1e2-203">PT_NULL o PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="5f1e2-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="5f1e2-204">**x**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-204">**x**</span></span> <br/> |<span data-ttu-id="5f1e2-205">LONG</span><span class="sxs-lookup"><span data-stu-id="5f1e2-205">LONG</span></span>  <br/> |
|<span data-ttu-id="5f1e2-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="5f1e2-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="5f1e2-207">**lpv**</span><span class="sxs-lookup"><span data-stu-id="5f1e2-207">**lpv**</span></span> <br/> |<span data-ttu-id="5f1e2-208">VOID \*</span><span class="sxs-lookup"><span data-stu-id="5f1e2-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f1e2-209">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f1e2-209">Remarks</span></span>

<span data-ttu-id="5f1e2-210">El **miembro ulPropTag** se conste de dos partes:</span><span class="sxs-lookup"><span data-stu-id="5f1e2-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="5f1e2-211">Un identificador de 16 bits de orden alto.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="5f1e2-212">Un tipo en orden bajo de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="5f1e2-213">El identificador es un valor numérico dentro de un intervalo determinado.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="5f1e2-214">MAPI define intervalos para que los identificadores describan para qué se usa la propiedad y quién es responsable de su mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="5f1e2-215">MAPI define restricciones para cada una de las etiquetas de propiedad que admite en el archivo de encabezado Mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="5f1e2-216">El tipo indica el formato del valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="5f1e2-217">MAPI define constantes para cada uno de los tipos de propiedad que admite en el archivo de encabezado Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="5f1e2-218">Para obtener una lista completa de los intervalos de propiedades válidos para identificadores y tipos de propiedad, vea el apéndice Identificadores y [tipos de](property-identifiers-and-types.md) propiedad.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="5f1e2-219">El **miembro dwAlignPad** se usa como espaciado interno para garantizar la alineación correcta en equipos que requieren alineación de 8 bytes para valores de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="5f1e2-220">Los desarrolladores que escriben código en estos equipos deben usar rutinas de asignación de memoria que asignen las matrices **SPropValue** en límites de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="5f1e2-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="5f1e2-221">Para obtener más información, vea [Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md) y actualización de propiedades [MAPI](updating-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="5f1e2-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5f1e2-222">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5f1e2-222">See also</span></span>



[<span data-ttu-id="5f1e2-223">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="5f1e2-223">MAPI Structures</span></span>](mapi-structures.md)

