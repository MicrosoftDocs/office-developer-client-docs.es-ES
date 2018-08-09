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
ms.openlocfilehash: f378bdd473410b846328cbe1f911eba9401f88cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820757"
---
# <a name="spropvalue"></a><span data-ttu-id="c0f23-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c0f23-103">SPropValue</span></span>

  
  
<span data-ttu-id="c0f23-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0f23-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0f23-105">Describe una propiedad MAPI.</span><span class="sxs-lookup"><span data-stu-id="c0f23-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0f23-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c0f23-106">Header file:</span></span>  <br/> |<span data-ttu-id="c0f23-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c0f23-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c0f23-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="c0f23-108">Related macros:</span></span>  <br/> |<span data-ttu-id="c0f23-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="c0f23-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="c0f23-110">Members</span><span class="sxs-lookup"><span data-stu-id="c0f23-110">Members</span></span>

 <span data-ttu-id="c0f23-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="c0f23-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="c0f23-112">Etiqueta de la propiedad para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c0f23-112">Property tag for the property.</span></span> <span data-ttu-id="c0f23-113">Las etiquetas de propiedad son enteros sin signo de 32 bits que consta del identificador único de la propiedad de orden superior a 16 bits y el tipo de propiedad de orden inferior a 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c0f23-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="c0f23-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="c0f23-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="c0f23-115">Reservado para MAPI; No use.</span><span class="sxs-lookup"><span data-stu-id="c0f23-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="c0f23-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c0f23-116">**Value**</span></span>
  
> <span data-ttu-id="c0f23-117">Unión de los valores de datos, el valor específico determinado por el tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c0f23-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="c0f23-118">En la siguiente tabla se enumera para cada tipo de propiedad, el miembro de la unión que se debe usar y su tipo de datos asociado.</span><span class="sxs-lookup"><span data-stu-id="c0f23-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="c0f23-119">**Tipo de propiedad**</span><span class="sxs-lookup"><span data-stu-id="c0f23-119">**Property type**</span></span>|<span data-ttu-id="c0f23-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c0f23-120">**Value**</span></span>|<span data-ttu-id="c0f23-121">**Tipo de datos del valor**</span><span class="sxs-lookup"><span data-stu-id="c0f23-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c0f23-122">PT_I2 o PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="c0f23-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="c0f23-123">**i**</span><span class="sxs-lookup"><span data-stu-id="c0f23-123">**i**</span></span> <br/> |<span data-ttu-id="c0f23-124">short int</span><span class="sxs-lookup"><span data-stu-id="c0f23-124">short int</span></span>  <br/> |
|<span data-ttu-id="c0f23-125">PT_I4 o PT_LONG (firmado)</span><span class="sxs-lookup"><span data-stu-id="c0f23-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="c0f23-126">**l**</span><span class="sxs-lookup"><span data-stu-id="c0f23-126">**l**</span></span> <br/> |<span data-ttu-id="c0f23-127">LARGO</span><span class="sxs-lookup"><span data-stu-id="c0f23-127">LONG</span></span>  <br/> |
|<span data-ttu-id="c0f23-128">PT_I4 o PT_LONG (sin firmar)</span><span class="sxs-lookup"><span data-stu-id="c0f23-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="c0f23-129">**UL**</span><span class="sxs-lookup"><span data-stu-id="c0f23-129">**ul**</span></span> <br/> |<span data-ttu-id="c0f23-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="c0f23-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="c0f23-131">PT_R4 o PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="c0f23-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="c0f23-132">**flt**</span><span class="sxs-lookup"><span data-stu-id="c0f23-132">**flt**</span></span> <br/> |<span data-ttu-id="c0f23-133">float</span><span class="sxs-lookup"><span data-stu-id="c0f23-133">float</span></span>  <br/> |
|<span data-ttu-id="c0f23-134">PT_R8 o PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="c0f23-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="c0f23-135">**doble**</span><span class="sxs-lookup"><span data-stu-id="c0f23-135">**dbl**</span></span> <br/> |<span data-ttu-id="c0f23-136">double</span><span class="sxs-lookup"><span data-stu-id="c0f23-136">double</span></span>  <br/> |
|<span data-ttu-id="c0f23-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c0f23-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="c0f23-138">**b**</span><span class="sxs-lookup"><span data-stu-id="c0f23-138">**b**</span></span> <br/> |<span data-ttu-id="c0f23-139">int corto sin firmar</span><span class="sxs-lookup"><span data-stu-id="c0f23-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="c0f23-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="c0f23-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="c0f23-141">**actual**</span><span class="sxs-lookup"><span data-stu-id="c0f23-141">**cur**</span></span> <br/> |[<span data-ttu-id="c0f23-142">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="c0f23-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="c0f23-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="c0f23-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="c0f23-144">**en**</span><span class="sxs-lookup"><span data-stu-id="c0f23-144">**at**</span></span> <br/> |<span data-ttu-id="c0f23-145">double</span><span class="sxs-lookup"><span data-stu-id="c0f23-145">double</span></span>  <br/> |
|<span data-ttu-id="c0f23-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c0f23-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="c0f23-147">**FT**</span><span class="sxs-lookup"><span data-stu-id="c0f23-147">**ft**</span></span> <br/> |[<span data-ttu-id="c0f23-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="c0f23-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="c0f23-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="c0f23-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="c0f23-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="c0f23-150">**lpszA**</span></span> <br/> |<span data-ttu-id="c0f23-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="c0f23-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="c0f23-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c0f23-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="c0f23-153">**Papelera de**</span><span class="sxs-lookup"><span data-stu-id="c0f23-153">**bin**</span></span> <br/> |<span data-ttu-id="c0f23-154">BYTE [matriz]</span><span class="sxs-lookup"><span data-stu-id="c0f23-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="c0f23-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c0f23-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="c0f23-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="c0f23-156">**lpszW**</span></span> <br/> |<span data-ttu-id="c0f23-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="c0f23-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="c0f23-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="c0f23-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="c0f23-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="c0f23-159">**lpguid**</span></span> <br/> |<span data-ttu-id="c0f23-160">LPGUID</span><span class="sxs-lookup"><span data-stu-id="c0f23-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="c0f23-161">PT_I8 o PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="c0f23-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="c0f23-162">**li**</span><span class="sxs-lookup"><span data-stu-id="c0f23-162">**li**</span></span> <br/> |<span data-ttu-id="c0f23-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="c0f23-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="c0f23-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="c0f23-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="c0f23-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="c0f23-165">**MVi**</span></span> <br/> |[<span data-ttu-id="c0f23-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="c0f23-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="c0f23-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="c0f23-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="c0f23-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="c0f23-168">**MVI**</span></span> <br/> |[<span data-ttu-id="c0f23-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="c0f23-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="c0f23-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="c0f23-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="c0f23-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="c0f23-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="c0f23-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="c0f23-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="c0f23-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="c0f23-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="c0f23-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="c0f23-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="c0f23-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="c0f23-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="c0f23-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="c0f23-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="c0f23-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="c0f23-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="c0f23-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="c0f23-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="c0f23-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="c0f23-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="c0f23-180">**MVat**</span><span class="sxs-lookup"><span data-stu-id="c0f23-180">**MVat**</span></span> <br/> |[<span data-ttu-id="c0f23-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="c0f23-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="c0f23-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="c0f23-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="c0f23-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="c0f23-183">**MVft**</span></span> <br/> |[<span data-ttu-id="c0f23-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="c0f23-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="c0f23-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="c0f23-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="c0f23-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="c0f23-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="c0f23-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="c0f23-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="c0f23-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="c0f23-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="c0f23-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="c0f23-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="c0f23-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="c0f23-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="c0f23-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c0f23-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="c0f23-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="c0f23-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="c0f23-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="c0f23-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="c0f23-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="c0f23-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="c0f23-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="c0f23-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="c0f23-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="c0f23-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="c0f23-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="c0f23-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="c0f23-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="c0f23-198">**MVli**</span></span> <br/> |[<span data-ttu-id="c0f23-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="c0f23-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="c0f23-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="c0f23-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="c0f23-201">**err**</span><span class="sxs-lookup"><span data-stu-id="c0f23-201">**err**</span></span> <br/> |[<span data-ttu-id="c0f23-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="c0f23-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="c0f23-203">PT_NULL o pt Object</span><span class="sxs-lookup"><span data-stu-id="c0f23-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="c0f23-204">**x**</span><span class="sxs-lookup"><span data-stu-id="c0f23-204">**x**</span></span> <br/> |<span data-ttu-id="c0f23-205">LARGO</span><span class="sxs-lookup"><span data-stu-id="c0f23-205">LONG</span></span>  <br/> |
|<span data-ttu-id="c0f23-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="c0f23-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="c0f23-207">**LPV**</span><span class="sxs-lookup"><span data-stu-id="c0f23-207">**lpv**</span></span> <br/> |<span data-ttu-id="c0f23-208">VOID\*</span><span class="sxs-lookup"><span data-stu-id="c0f23-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0f23-209">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c0f23-209">Remarks</span></span>

<span data-ttu-id="c0f23-210">El miembro **ulPropTag** se compone de dos partes:</span><span class="sxs-lookup"><span data-stu-id="c0f23-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="c0f23-211">Un identificador de orden superior a 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c0f23-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="c0f23-212">Un tipo de orden inferior a 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c0f23-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="c0f23-213">El identificador es un valor numérico dentro de un intervalo determinado.</span><span class="sxs-lookup"><span data-stu-id="c0f23-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="c0f23-214">MAPI define los intervalos para los identificadores describir la propiedad que se usa para y quién es responsable de mantenerlo.</span><span class="sxs-lookup"><span data-stu-id="c0f23-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="c0f23-215">MAPI define restricciones para cada una de las etiquetas de propiedad que admite en el archivo de encabezado Mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="c0f23-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="c0f23-216">El tipo indica el formato para el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c0f23-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="c0f23-217">MAPI define constantes para cada uno de los tipos de propiedad que admite en el archivo de encabezado Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="c0f23-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="c0f23-218">Para obtener una lista completa de los intervalos de propiedad válido para los identificadores y tipos de propiedad, consulte el apéndice [identificadores de propiedades y tipos](property-identifiers-and-types.md) .</span><span class="sxs-lookup"><span data-stu-id="c0f23-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="c0f23-219">El miembro **dwAlignPad** se utiliza como relleno para realizar la alineación adecuada seguro en los equipos que requieren la alineación de 8 bytes para los valores de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="c0f23-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="c0f23-220">Los desarrolladores que escribir código en estos equipos deben utilizar rutinas de asignación de memoria que asignan las matrices **SPropValue** en límites de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="c0f23-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="c0f23-221">Para obtener más información, vea [Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md) y [Actualizar las propiedades de MAPI](updating-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="c0f23-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c0f23-222">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0f23-222">See also</span></span>



[<span data-ttu-id="c0f23-223">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="c0f23-223">MAPI Structures</span></span>](mapi-structures.md)

