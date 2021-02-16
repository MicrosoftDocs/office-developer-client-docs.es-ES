---
title: Ejemplo de secuencia folderUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e5251a619c70221987847830897ba349d63fd9cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433979"
---
# <a name="folderuserfields-stream-sample"></a><span data-ttu-id="ecba2-103">Ejemplo de secuencia folderUserFields</span><span class="sxs-lookup"><span data-stu-id="ecba2-103">FolderUserFields stream sample</span></span>

<span data-ttu-id="ecba2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecba2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecba2-105">En este tema se describe un ejemplo de una secuencia FolderUserFields.</span><span class="sxs-lookup"><span data-stu-id="ecba2-105">This topic describes an example of a FolderUserFields stream.</span></span> <span data-ttu-id="ecba2-106">La secuencia contiene una definición de un campo definido por el usuario,  `TextField1` .</span><span class="sxs-lookup"><span data-stu-id="ecba2-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="ecba2-107">El tipo es **Texto** y la secuencia FolderUserFields contiene las partes FolderUserFieldsAnsi y FolderUserFieldsUnicode.</span><span class="sxs-lookup"><span data-stu-id="ecba2-107">The type is **Text**, and the FolderUserFields stream contains both FolderUserFieldsAnsi and FolderUserFieldsUnicode parts.</span></span> <span data-ttu-id="ecba2-108">Para obtener más información, [vea Estructuras de secuencia de campos de carpeta.](folder-fields-stream-structures.md)</span><span class="sxs-lookup"><span data-stu-id="ecba2-108">For more information see [Folder Fields Stream Structures](folder-fields-stream-structures.md).</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="ecba2-109">Volcado de datos</span><span class="sxs-lookup"><span data-stu-id="ecba2-109">Data dump</span></span>

<span data-ttu-id="ecba2-110">A continuación se muestra un volcado de datos de la secuencia tal como se mostraría en un editor binario.</span><span class="sxs-lookup"><span data-stu-id="ecba2-110">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="ecba2-111">Desplazamiento de la secuencia</span><span class="sxs-lookup"><span data-stu-id="ecba2-111">Stream offset</span></span>|<span data-ttu-id="ecba2-112">Bytes de datos</span><span class="sxs-lookup"><span data-stu-id="ecba2-112">Data bytes</span></span>|<span data-ttu-id="ecba2-113">Datos ASCII</span><span class="sxs-lookup"><span data-stu-id="ecba2-113">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `02 00 00 00 01 00 00 00 0A 00 54 65 78 74 46 69` <br/> | `..........TextFi` <br/> |
| `0000000010` <br/> | `65 6C 64 31 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `eld1).......A...` <br/> |
| `0000000020` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `0000000030` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000040` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000050` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000060` <br/> | `00 00 00 00 00 00 02 00 00 00 01 00 00 00 0A 00` <br/> | `................` <br/> |
| `0000000070` <br/> | `54 00 65 00 78 00 74 00 46 00 69 00 65 00 6C 00` <br/> | `T.e.x.t.F.i.e.l.` <br/> |
| `0000000080` <br/> | `64 00 31 00 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `d.1.).......A...` <br/> |
| `0000000090` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `00000000A0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000B0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000C0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000D0` <br/> | `00 00 00 00 00 00` <br/> | `......` <br/> |
   

<span data-ttu-id="ecba2-114">A continuación se muestra un análisis de los datos de ejemplo para la secuencia **FolderUserFields:**</span><span class="sxs-lookup"><span data-stu-id="ecba2-114">The following is a parse of the sample data for the **FolderUserFields** stream:</span></span>
  
- <span data-ttu-id="ecba2-115">FolderUserFieldsAnsi: desplazamiento 0x0.</span><span class="sxs-lookup"><span data-stu-id="ecba2-115">FolderUserFieldsAnsi: Offset 0x0.</span></span>
    
  - <span data-ttu-id="ecba2-116">FieldDefinitionCount: desplazamiento 0x0, 4 bytes: 0x00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="ecba2-116">FieldDefinitionCount: Offset 0x0, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="ecba2-117">FieldDefinitions: desplazamiento 0x4, matriz de 2 secuencias FolderFieldDefinitionA.</span><span class="sxs-lookup"><span data-stu-id="ecba2-117">FieldDefinitions: Offset 0x4, array of 2 FolderFieldDefinitionA streams.</span></span>
    
    <span data-ttu-id="ecba2-118">**Primer elemento de matriz:**</span><span class="sxs-lookup"><span data-stu-id="ecba2-118">**First array element**:</span></span>
    
    - <span data-ttu-id="ecba2-119">FieldType: desplazamiento 0x4, 4 bytes: 0x00000001 (ftString).</span><span class="sxs-lookup"><span data-stu-id="ecba2-119">FieldType: Offset 0x4, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="ecba2-120">FieldNameLength: desplazamiento 0x8, 2 bytes: 0x000A (10)</span><span class="sxs-lookup"><span data-stu-id="ecba2-120">FieldNameLength: Offset 0x8, 2 bytes: 0x000A (10)</span></span>
      
    - <span data-ttu-id="ecba2-121">FieldName: desplazamiento 0xA, matriz de 10 MATRIZ.</span><span class="sxs-lookup"><span data-stu-id="ecba2-121">FieldName: Offset 0xA, array of 10 CHARs.</span></span> <span data-ttu-id="ecba2-122">Valor de cadena ANSI: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="ecba2-122">ANSI string value: "TextField1".</span></span>
      
    - <span data-ttu-id="ecba2-123">Común: desplazamiento 0x14.</span><span class="sxs-lookup"><span data-stu-id="ecba2-123">Common: Offset 0x14.</span></span>
    
      - <span data-ttu-id="ecba2-124">PropSetGuid: desplazamiento 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="ecba2-124">PropSetGuid: Offset 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="ecba2-125">fcapm: desplazamiento 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP| FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="ecba2-125">fcapm: Offset 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="ecba2-126">dwString: desplazamiento 0x28, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ecba2-126">dwString: Offset 0x28, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="ecba2-127">dwBitmap: desplazamiento 0x2C, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ecba2-127">dwBitmap: Offset 0x2C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="ecba2-128">dwDisplay: desplazamiento 0x30, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ecba2-128">dwDisplay: Offset 0x30, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="ecba2-129">iFmt: desplazamiento 0x34, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ecba2-129">iFmt: Offset 0x34, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="ecba2-130">wszFormulaLength: desplazamiento 0x38, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="ecba2-130">wszFormulaLength: Offset 0x38, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="ecba2-131">wszFormula: desplazamiento 0x3A, matriz de 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="ecba2-131">wszFormula: Offset 0x3A, array of 0 WCHARs.</span></span> <span data-ttu-id="ecba2-132">Valor de cadena vacío.</span><span class="sxs-lookup"><span data-stu-id="ecba2-132">Empty string value.</span></span>
    
    <span data-ttu-id="ecba2-133">**Segundo elemento de matriz:**</span><span class="sxs-lookup"><span data-stu-id="ecba2-133">**Second array element**:</span></span>
    
    - <span data-ttu-id="ecba2-134">FieldType: desplazamiento 0x3A, 4 bytes: 0x00000000 (ftNone).</span><span class="sxs-lookup"><span data-stu-id="ecba2-134">FieldType: Offset 0x3A, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="ecba2-135">FieldNameLength: desplazamiento 0x3E, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="ecba2-135">FieldNameLength: Offset 0x3E, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="ecba2-136">FieldName: desplazamiento 0x40, matriz de 0 CHAR.</span><span class="sxs-lookup"><span data-stu-id="ecba2-136">FieldName: Offset 0x40, array of 0 CHARs.</span></span> <span data-ttu-id="ecba2-137">Valor de cadena vacío.</span><span class="sxs-lookup"><span data-stu-id="ecba2-137">Empty string value.</span></span>
      
    - <span data-ttu-id="ecba2-138">Común: desplazamiento 0x40.</span><span class="sxs-lookup"><span data-stu-id="ecba2-138">Common: Offset 0x40.</span></span>
    
      - <span data-ttu-id="ecba2-139">PropSetGuid: desplazamiento 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="ecba2-139">PropSetGuid: Offset 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="ecba2-140">fcapm: desplazamiento 0x50, 4 bytes: 0x00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="ecba2-140">fcapm: Offset 0x50, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="ecba2-141">dwString: desplazamiento 0x54, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ecba2-141">dwString: Offset 0x54, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="ecba2-142">dwBitmap: desplazamiento 0x58, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ecba2-142">dwBitmap: Offset 0x58, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="ecba2-143">dwDisplay: desplazamiento 0x5C, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ecba2-143">dwDisplay: Offset 0x5C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="ecba2-144">iFmt: desplazamiento 0x60, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ecba2-144">iFmt: Offset 0x60, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="ecba2-145">wszFormulaLength: desplazamiento 0x64, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="ecba2-145">wszFormulaLength: Offset 0x64, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="ecba2-146">wszFormula: desplazamiento 0x66, matriz de 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="ecba2-146">wszFormula: Offset 0x66, array of 0 WCHARs.</span></span> <span data-ttu-id="ecba2-147">Valor de cadena vacío.</span><span class="sxs-lookup"><span data-stu-id="ecba2-147">Empty string value.</span></span>
    
- <span data-ttu-id="ecba2-148">FolderUserFieldsUnicode: desplazamiento 0x66.</span><span class="sxs-lookup"><span data-stu-id="ecba2-148">FolderUserFieldsUnicode: Offset 0x66.</span></span>
    
  - <span data-ttu-id="ecba2-149">FieldDefinitionCount: desplazamiento 0x66, 4 bytes: 0x00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="ecba2-149">FieldDefinitionCount: Offset 0x66, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="ecba2-150">FieldDefinitions: desplazamiento 0x6A, matriz de 2 secuencias FolderFieldDefinitionW.</span><span class="sxs-lookup"><span data-stu-id="ecba2-150">FieldDefinitions: Offset 0x6A, array of 2 FolderFieldDefinitionW streams.</span></span>
    
    <span data-ttu-id="ecba2-151">**Primer elemento de matriz:**</span><span class="sxs-lookup"><span data-stu-id="ecba2-151">**First array element**:</span></span>
    
    - <span data-ttu-id="ecba2-152">FieldType: desplazamiento 0x6A, 4 bytes: 0x00000001 (ftString).</span><span class="sxs-lookup"><span data-stu-id="ecba2-152">FieldType: Offset 0x6A, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="ecba2-153">FieldNameLength: desplazamiento 0x6E, 2 bytes: 0x000A (10).</span><span class="sxs-lookup"><span data-stu-id="ecba2-153">FieldNameLength: Offset 0x6E, 2 bytes: 0x000A (10).</span></span>
      
    - <span data-ttu-id="ecba2-154">FieldName: desplazamiento 0x70, matriz de 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="ecba2-154">FieldName: Offset 0x70, array of 10 WCHARs.</span></span> <span data-ttu-id="ecba2-155">Valor de cadena Unicode: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="ecba2-155">Unicode string value: "TextField1".</span></span>
      
    - <span data-ttu-id="ecba2-156">Común: desplazamiento 0x84.</span><span class="sxs-lookup"><span data-stu-id="ecba2-156">Common: Offset 0x84.</span></span>
    
      - <span data-ttu-id="ecba2-157">PropSetGuid: desplazamiento 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="ecba2-157">PropSetGuid: Offset 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="ecba2-158">fcapm: desplazamiento 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP| FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="ecba2-158">fcapm: Offset 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="ecba2-159">dwString: desplazamiento 0x98, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ecba2-159">dwString: Offset 0x98, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="ecba2-160">dwBitmap: desplazamiento 0x9C, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ecba2-160">dwBitmap: Offset 0x9C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="ecba2-161">dwDisplay: desplazamiento 0xA0, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ecba2-161">dwDisplay: Offset 0xA0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="ecba2-162">iFmt: desplazamiento 0xA4, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ecba2-162">iFmt: Offset 0xA4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="ecba2-163">wszFormulaLength: desplazamiento 0xA8, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="ecba2-163">wszFormulaLength: Offset 0xA8, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="ecba2-164">wszFormula: desplazamiento 0xAA, matriz de 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="ecba2-164">wszFormula: Offset 0xAA, array of 0 WCHARs.</span></span> <span data-ttu-id="ecba2-165">Valor de cadena vacío.</span><span class="sxs-lookup"><span data-stu-id="ecba2-165">Empty string value.</span></span>
    
    <span data-ttu-id="ecba2-166">**Segundo elemento de matriz:**</span><span class="sxs-lookup"><span data-stu-id="ecba2-166">**Second array element**:</span></span>
    
    - <span data-ttu-id="ecba2-167">FieldType: desplazamiento 0xAA, 4 bytes: 0x00000000 (ftNone).</span><span class="sxs-lookup"><span data-stu-id="ecba2-167">FieldType: Offset 0xAA, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="ecba2-168">FieldNameLength: desplazamiento 0xAE, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="ecba2-168">FieldNameLength: Offset 0xAE, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="ecba2-169">FieldName: desplazamiento 0xB0, matriz de 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="ecba2-169">FieldName: Offset 0xB0, array of 0 WCHARs.</span></span> <span data-ttu-id="ecba2-170">Valor de cadena vacío.</span><span class="sxs-lookup"><span data-stu-id="ecba2-170">Empty string value.</span></span>
      
    - <span data-ttu-id="ecba2-171">Común: desplazamiento 0xB0.</span><span class="sxs-lookup"><span data-stu-id="ecba2-171">Common: Offset 0xB0.</span></span>
    
      - <span data-ttu-id="ecba2-172">PropSetGuid: desplazamiento 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="ecba2-172">PropSetGuid: Offset 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="ecba2-173">fcapm: desplazamiento 0xC0, 4 bytes: 0x00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="ecba2-173">fcapm: Offset 0xC0, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="ecba2-174">dwString: desplazamiento 0xC4, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ecba2-174">dwString: Offset 0xC4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="ecba2-175">dwBitmap: desplazamiento 0xC8, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ecba2-175">dwBitmap: Offset 0xC8, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="ecba2-176">dwDisplay: desplazamiento 0xCC, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ecba2-176">dwDisplay: Offset 0xCC, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="ecba2-177">iFmt: desplazamiento 0xD0, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="ecba2-177">iFmt: Offset 0xD0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="ecba2-178">wszFormulaLength: desplazamiento 0xD4, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="ecba2-178">wszFormulaLength: Offset 0xD4, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="ecba2-179">wszFormula: desplazamiento 0xD6, matriz de 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="ecba2-179">wszFormula: Offset 0xD6, array of 0 WCHARs.</span></span> <span data-ttu-id="ecba2-180">Valor de cadena vacío.</span><span class="sxs-lookup"><span data-stu-id="ecba2-180">Empty string value.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ecba2-181">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ecba2-181">See also</span></span>

- [<span data-ttu-id="ecba2-182">Elementos y campos de Outlook</span><span class="sxs-lookup"><span data-stu-id="ecba2-182">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="ecba2-183">Estructura de secuencia PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="ecba2-183">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="ecba2-184">Estructura de secuencia FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="ecba2-184">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="ecba2-185">Estructura de flujo SkipBlock</span><span class="sxs-lookup"><span data-stu-id="ecba2-185">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="ecba2-186">Estructura de secuencia FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="ecba2-186">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="ecba2-187">Estructura de secuencias PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="ecba2-187">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="ecba2-188">Estructura de secuencias PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="ecba2-188">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

