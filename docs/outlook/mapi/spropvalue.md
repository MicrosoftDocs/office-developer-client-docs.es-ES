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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326589"
---
# <a name="spropvalue"></a><span data-ttu-id="c8d6b-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c8d6b-103">SPropValue</span></span>

  
  
<span data-ttu-id="c8d6b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8d6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8d6b-105">Describe una propiedad MAPI.</span><span class="sxs-lookup"><span data-stu-id="c8d6b-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8d6b-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c8d6b-106">Header file:</span></span>  <br/> |<span data-ttu-id="c8d6b-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c8d6b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c8d6b-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="c8d6b-108">Related macros:</span></span>  <br/> |<span data-ttu-id="c8d6b-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="c8d6b-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="c8d6b-110">Members</span><span class="sxs-lookup"><span data-stu-id="c8d6b-110">Members</span></span>

 <span data-ttu-id="c8d6b-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="c8d6b-112">Etiqueta de propiedad de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c8d6b-112">Property tag for the property.</span></span> <span data-ttu-id="c8d6b-113">Las etiquetas de propiedad son enteros sin signo de 32 bits que constan del identificador único de la propiedad en los 16 bits de orden superior y el tipo de la propiedad en los 16 bits de orden inferior.</span><span class="sxs-lookup"><span data-stu-id="c8d6b-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="c8d6b-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="c8d6b-115">Reservado para MAPI; No use.</span><span class="sxs-lookup"><span data-stu-id="c8d6b-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="c8d6b-116">**Value**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-116">**Value**</span></span>
  
> <span data-ttu-id="c8d6b-117">Unión de valores de datos, el valor específico que dicta el tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c8d6b-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="c8d6b-118">En la tabla siguiente se enumeran para cada tipo de propiedad, el miembro de la Unión que se debe usar y su tipo de datos asociado.</span><span class="sxs-lookup"><span data-stu-id="c8d6b-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="c8d6b-119">**Tipo de propiedad**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-119">**Property type**</span></span>|<span data-ttu-id="c8d6b-120">**Value**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-120">**Value**</span></span>|<span data-ttu-id="c8d6b-121">**Tipo de datos de valor**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c8d6b-122">PT_I2 o PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="c8d6b-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="c8d6b-123">**sigo**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-123">**i**</span></span> <br/> |<span data-ttu-id="c8d6b-124">short int</span><span class="sxs-lookup"><span data-stu-id="c8d6b-124">short int</span></span>  <br/> |
|<span data-ttu-id="c8d6b-125">PT_I4 o PT_LONG (con signo)</span><span class="sxs-lookup"><span data-stu-id="c8d6b-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="c8d6b-126">**l**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-126">**l**</span></span> <br/> |<span data-ttu-id="c8d6b-127">DESDE</span><span class="sxs-lookup"><span data-stu-id="c8d6b-127">LONG</span></span>  <br/> |
|<span data-ttu-id="c8d6b-128">PT_I4 o PT_LONG (sin asignar)</span><span class="sxs-lookup"><span data-stu-id="c8d6b-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="c8d6b-129">**UL**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-129">**ul**</span></span> <br/> |<span data-ttu-id="c8d6b-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="c8d6b-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="c8d6b-131">PT_R4 o PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="c8d6b-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="c8d6b-132">**FLT**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-132">**flt**</span></span> <br/> |<span data-ttu-id="c8d6b-133">float</span><span class="sxs-lookup"><span data-stu-id="c8d6b-133">float</span></span>  <br/> |
|<span data-ttu-id="c8d6b-134">PT_R8 o PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="c8d6b-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="c8d6b-135">**japonesa**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-135">**dbl**</span></span> <br/> |<span data-ttu-id="c8d6b-136">double</span><span class="sxs-lookup"><span data-stu-id="c8d6b-136">double</span></span>  <br/> |
|<span data-ttu-id="c8d6b-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c8d6b-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="c8d6b-138">**b**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-138">**b**</span></span> <br/> |<span data-ttu-id="c8d6b-139">unsigned short int</span><span class="sxs-lookup"><span data-stu-id="c8d6b-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="c8d6b-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="c8d6b-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="c8d6b-141">**Espacia**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-141">**cur**</span></span> <br/> |[<span data-ttu-id="c8d6b-142">Visa</span><span class="sxs-lookup"><span data-stu-id="c8d6b-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="c8d6b-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="c8d6b-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="c8d6b-144">**Veamos**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-144">**at**</span></span> <br/> |<span data-ttu-id="c8d6b-145">double</span><span class="sxs-lookup"><span data-stu-id="c8d6b-145">double</span></span>  <br/> |
|<span data-ttu-id="c8d6b-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c8d6b-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="c8d6b-147">**cm**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-147">**ft**</span></span> <br/> |[<span data-ttu-id="c8d6b-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="c8d6b-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="c8d6b-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="c8d6b-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="c8d6b-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-150">**lpszA**</span></span> <br/> |<span data-ttu-id="c8d6b-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="c8d6b-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="c8d6b-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c8d6b-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="c8d6b-153">**definido**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-153">**bin**</span></span> <br/> |<span data-ttu-id="c8d6b-154">BYTE [matriz]</span><span class="sxs-lookup"><span data-stu-id="c8d6b-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="c8d6b-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c8d6b-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="c8d6b-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-156">**lpszW**</span></span> <br/> |<span data-ttu-id="c8d6b-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="c8d6b-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="c8d6b-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="c8d6b-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="c8d6b-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-159">**lpguid**</span></span> <br/> |<span data-ttu-id="c8d6b-160">LPGUID</span><span class="sxs-lookup"><span data-stu-id="c8d6b-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="c8d6b-161">PT_I8 o PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="c8d6b-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="c8d6b-162">**Li**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-162">**li**</span></span> <br/> |<span data-ttu-id="c8d6b-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="c8d6b-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="c8d6b-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="c8d6b-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-165">**MVi**</span></span> <br/> |[<span data-ttu-id="c8d6b-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="c8d6b-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="c8d6b-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="c8d6b-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="c8d6b-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-168">**MVI**</span></span> <br/> |[<span data-ttu-id="c8d6b-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="c8d6b-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="c8d6b-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="c8d6b-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="c8d6b-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="c8d6b-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="c8d6b-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="c8d6b-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="c8d6b-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="c8d6b-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="c8d6b-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="c8d6b-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="c8d6b-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="c8d6b-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="c8d6b-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="c8d6b-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="c8d6b-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="c8d6b-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="c8d6b-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="c8d6b-180">**MVat**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-180">**MVat**</span></span> <br/> |[<span data-ttu-id="c8d6b-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="c8d6b-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="c8d6b-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c8d6b-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="c8d6b-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-183">**MVft**</span></span> <br/> |[<span data-ttu-id="c8d6b-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="c8d6b-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="c8d6b-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="c8d6b-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="c8d6b-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="c8d6b-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="c8d6b-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="c8d6b-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="c8d6b-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="c8d6b-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="c8d6b-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="c8d6b-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="c8d6b-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c8d6b-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="c8d6b-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="c8d6b-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="c8d6b-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="c8d6b-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="c8d6b-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="c8d6b-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="c8d6b-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="c8d6b-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="c8d6b-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="c8d6b-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="c8d6b-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-198">**MVli**</span></span> <br/> |[<span data-ttu-id="c8d6b-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="c8d6b-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="c8d6b-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="c8d6b-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="c8d6b-201">**err**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-201">**err**</span></span> <br/> |[<span data-ttu-id="c8d6b-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="c8d6b-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="c8d6b-203">PT_NULL o PT Object</span><span class="sxs-lookup"><span data-stu-id="c8d6b-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="c8d6b-204">**x**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-204">**x**</span></span> <br/> |<span data-ttu-id="c8d6b-205">DESDE</span><span class="sxs-lookup"><span data-stu-id="c8d6b-205">LONG</span></span>  <br/> |
|<span data-ttu-id="c8d6b-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="c8d6b-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="c8d6b-207">**LPV**</span><span class="sxs-lookup"><span data-stu-id="c8d6b-207">**lpv**</span></span> <br/> |<span data-ttu-id="c8d6b-208">EFECTO\*</span><span class="sxs-lookup"><span data-stu-id="c8d6b-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8d6b-209">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c8d6b-209">Remarks</span></span>

<span data-ttu-id="c8d6b-210">El miembro **ulPropTag** está formado por dos partes:</span><span class="sxs-lookup"><span data-stu-id="c8d6b-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="c8d6b-211">Un identificador en los 16 bits de orden superior.</span><span class="sxs-lookup"><span data-stu-id="c8d6b-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="c8d6b-212">Un tipo en los 16 bits de orden inferior.</span><span class="sxs-lookup"><span data-stu-id="c8d6b-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="c8d6b-213">El identificador es un valor numérico dentro de un intervalo determinado.</span><span class="sxs-lookup"><span data-stu-id="c8d6b-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="c8d6b-214">MAPI define los intervalos de los identificadores para describir para qué se usa la propiedad y quién es responsable de su mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="c8d6b-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="c8d6b-215">MAPI define restricciones para cada una de las etiquetas de propiedad que admite en el archivo de encabezado Mapitags. h.</span><span class="sxs-lookup"><span data-stu-id="c8d6b-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="c8d6b-216">El tipo indica el formato del valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c8d6b-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="c8d6b-217">MAPI define constantes para cada uno de los tipos de propiedad que admite en el archivo de encabezado Mapidefs. h.</span><span class="sxs-lookup"><span data-stu-id="c8d6b-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="c8d6b-218">Para obtener una lista completa de los intervalos de propiedades válidos para los identificadores y tipos de propiedades, vea el apéndice [identificadores y tipos de propiedades](property-identifiers-and-types.md) .</span><span class="sxs-lookup"><span data-stu-id="c8d6b-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="c8d6b-219">El miembro **dwAlignPad** se usa como relleno para garantizar una alineación adecuada en los equipos que requieren una alineación de 8 bytes para los valores de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="c8d6b-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="c8d6b-220">Los desarrolladores que escriben código en estos equipos deben usar rutinas de asignación de memoria que asignan las matrices de **SPropValue** en límites de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="c8d6b-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="c8d6b-221">Para obtener más información, consulte [información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md) y [actualizar las propiedades MAPI](updating-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="c8d6b-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c8d6b-222">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8d6b-222">See also</span></span>



[<span data-ttu-id="c8d6b-223">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="c8d6b-223">MAPI Structures</span></span>](mapi-structures.md)

