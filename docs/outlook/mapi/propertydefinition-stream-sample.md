---
title: Ejemplo de secuencia PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 63a8141221c0ff7a8c6ffee20587b682386f87b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406664"
---
# <a name="propertydefinition-stream-sample"></a><span data-ttu-id="115ea-103">Ejemplo de secuencia PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="115ea-103">PropertyDefinition stream sample</span></span>

<span data-ttu-id="115ea-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="115ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="115ea-105">En este tema se describe un ejemplo de una secuencia PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="115ea-105">This topic describes an example of a PropertyDefinition stream.</span></span> <span data-ttu-id="115ea-106">La secuencia contiene una definición de un campo definido por el usuario,  `TextField1` .</span><span class="sxs-lookup"><span data-stu-id="115ea-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="115ea-107">El tipo es **Text** y la definición tiene el formato PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="115ea-107">The type is **Text**, and the definition is in the PropDefV2 format.</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="115ea-108">Volcado de datos</span><span class="sxs-lookup"><span data-stu-id="115ea-108">Data dump</span></span>

<span data-ttu-id="115ea-109">A continuación se muestra un volcado de datos de la secuencia tal como se mostraría en un editor binario.</span><span class="sxs-lookup"><span data-stu-id="115ea-109">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="115ea-110">Desplazamiento de secuencia</span><span class="sxs-lookup"><span data-stu-id="115ea-110">Stream offset</span></span>|<span data-ttu-id="115ea-111">Bytes de datos</span><span class="sxs-lookup"><span data-stu-id="115ea-111">Data bytes</span></span>|<span data-ttu-id="115ea-112">Datos ASCII</span><span class="sxs-lookup"><span data-stu-id="115ea-112">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
<span data-ttu-id="115ea-113">A continuación se muestra un análisis de los datos de ejemplo de la secuencia PropertyDefinition:</span><span class="sxs-lookup"><span data-stu-id="115ea-113">The following is a parse of the sample data for the PropertyDefinition stream:</span></span>
  
- <span data-ttu-id="115ea-114">Versión: desplazamiento 0x0, 2 bytes: 0x0103 (PropDefV2).</span><span class="sxs-lookup"><span data-stu-id="115ea-114">Version: Offset 0x0, 2 bytes: 0x0103 (PropDefV2).</span></span>
    
- <span data-ttu-id="115ea-115">FieldDefinitionCount: desplazamiento 0x2, 4 bytes: 0x1 (1).</span><span class="sxs-lookup"><span data-stu-id="115ea-115">FieldDefinitionCount: Offset 0x2, 4 bytes: 0x1 (1).</span></span>
    
- <span data-ttu-id="115ea-116">FieldDefinitions: desplazamiento 0x6, matriz de 1 secuencia FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="115ea-116">FieldDefinitions: Offset 0x6, array of 1 FieldDefinition stream.</span></span>
    
  - <span data-ttu-id="115ea-117">Marcas: desplazamiento 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM| PDO_PRINT_SAVEAS| PDO_PRINT_SAVEAS_DEF).</span><span class="sxs-lookup"><span data-stu-id="115ea-117">Flags: Offset 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM|PDO_PRINT_SAVEAS|PDO_PRINT_SAVEAS_DEF).</span></span>
    
  - <span data-ttu-id="115ea-118">VT: desplazamiento 0xA, 2 bytes: 0x8 (**VT_BSTR**).</span><span class="sxs-lookup"><span data-stu-id="115ea-118">VT: Offset 0xA, 2 bytes: 0x8 (**VT_BSTR**).</span></span>
    
  - <span data-ttu-id="115ea-119">DispId: desplazamiento 0xC, 4 bytes: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="115ea-119">DispId: Offset 0xC, 4 bytes: 0x0 (0).</span></span>
    
  - <span data-ttu-id="115ea-120">NmidNameLength: desplazamiento 0x10, 2 bytes: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="115ea-120">NmidNameLength: Offset 0x10, 2 bytes: 0xA (10).</span></span>
    
  - <span data-ttu-id="115ea-121">NmidName: offset 0x12, matriz de 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="115ea-121">NmidName: Offset 0x12, array of 10 WCHARs.</span></span> <span data-ttu-id="115ea-122">Valor de cadena Unicode: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="115ea-122">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="115ea-123">NameANSI: desplazamiento 0x26, secuencia PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="115ea-123">NameANSI: Offset 0x26, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="115ea-124">Length: Offset 0x26, 1 byte: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="115ea-124">Length: Offset 0x26, 1 byte: 0xA (10).</span></span>
      
    - <span data-ttu-id="115ea-125">Caracteres: desplazamiento 0x27, matriz de 10 RS.</span><span class="sxs-lookup"><span data-stu-id="115ea-125">Characters: Offset 0x27, array of 10 CHARs.</span></span> <span data-ttu-id="115ea-126">Valor de cadena ANSI: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="115ea-126">ANSI string value: "TextField1".</span></span>
    
  - <span data-ttu-id="115ea-127">FormulaANSI: desplazamiento 0x31, secuencia PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="115ea-127">FormulaANSI: Offset 0x31, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="115ea-128">Length: Offset 0x31, 1 byte: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="115ea-128">Length: Offset 0x31, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="115ea-129">Caracteres: desplazamiento 0x32, matriz de 0 RS.</span><span class="sxs-lookup"><span data-stu-id="115ea-129">Characters: Offset 0x32, array of 0 CHARs.</span></span> <span data-ttu-id="115ea-130">Cadena ANSI vacía.</span><span class="sxs-lookup"><span data-stu-id="115ea-130">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="115ea-131">ValidationRuleANSI: desplazamiento 0x32, secuencia PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="115ea-131">ValidationRuleANSI: Offset 0x32, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="115ea-132">Length: Offset 0x32, 1 byte: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="115ea-132">Length: Offset 0x32, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="115ea-133">Caracteres: desplazamiento 0x33, matriz de 0 CHAR.</span><span class="sxs-lookup"><span data-stu-id="115ea-133">Characters: Offset 0x33, array of 0 CHARs.</span></span> <span data-ttu-id="115ea-134">Cadena ANSI vacía.</span><span class="sxs-lookup"><span data-stu-id="115ea-134">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="115ea-135">ValidationTextANSI: desplazamiento 0x33, secuencia PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="115ea-135">ValidationTextANSI: Offset 0x33, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="115ea-136">Length: Offset 0x33, 1 byte: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="115ea-136">Length: Offset 0x33, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="115ea-137">Caracteres: desplazamiento 0x34, matriz de 0 RS.</span><span class="sxs-lookup"><span data-stu-id="115ea-137">Characters: Offset 0x34, array of 0 CHARs.</span></span> <span data-ttu-id="115ea-138">Cadena ANSI vacía.</span><span class="sxs-lookup"><span data-stu-id="115ea-138">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="115ea-139">ErrorANSI: desplazamiento 0x34, secuencia PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="115ea-139">ErrorANSI: Offset 0x34, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="115ea-140">Length: Offset 0x34, 1 byte: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="115ea-140">Length: Offset 0x34, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="115ea-141">Caracteres: desplazamiento 0x35, matriz de 0 RS.</span><span class="sxs-lookup"><span data-stu-id="115ea-141">Characters: Offset 0x35, array of 0 CHARs.</span></span> <span data-ttu-id="115ea-142">Cadena ANSI vacía.</span><span class="sxs-lookup"><span data-stu-id="115ea-142">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="115ea-143">InternalType: Desplazamiento 0x35, 4 bytes: 0x0 (iTypeString).</span><span class="sxs-lookup"><span data-stu-id="115ea-143">InternalType: Offset 0x35, 4 bytes: 0x0 (iTypeString).</span></span>
    
  - <span data-ttu-id="115ea-144">SkipBlocks: desplazamiento 0x39, serie de secuencias SkipBlock.</span><span class="sxs-lookup"><span data-stu-id="115ea-144">SkipBlocks: Offset 0x39, series of SkipBlock streams.</span></span>
    
  - <span data-ttu-id="115ea-145">First SkipBlock</span><span class="sxs-lookup"><span data-stu-id="115ea-145">First SkipBlock</span></span>
    
    - <span data-ttu-id="115ea-146">Tamaño: desplazamiento 0x39, 4 bytes: 0x15 (21).</span><span class="sxs-lookup"><span data-stu-id="115ea-146">Size: Offset 0x39, 4 bytes: 0x15 (21).</span></span>
      
    - <span data-ttu-id="115ea-147">Contenido: desplazamiento 0x3D, matriz de 21 bytes.</span><span class="sxs-lookup"><span data-stu-id="115ea-147">Content: Offset 0x3D, array of 21 bytes.</span></span> <span data-ttu-id="115ea-148">Esta es la primera secuencia SkipBlock, por lo que esta matriz contiene una secuencia FirstSkipBlockContent.</span><span class="sxs-lookup"><span data-stu-id="115ea-148">This is the first SkipBlock stream, so this array contains a FirstSkipBlockContent stream.</span></span>
      
      - <span data-ttu-id="115ea-149">FieldName: Offset 0x3D, secuencia PackedUnicodeString.</span><span class="sxs-lookup"><span data-stu-id="115ea-149">FieldName: Offset 0x3D, PackedUnicodeString stream.</span></span>
        
        - <span data-ttu-id="115ea-150">Length: Offset 0x3D, 1 byte: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="115ea-150">Length: Offset 0x3D, 1 byte: 0xA (10).</span></span>
          
        - <span data-ttu-id="115ea-151">Caracteres: desplazamiento 0x3E, matriz de 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="115ea-151">Characters: Offset 0x3E, array of 10 WCHARs.</span></span> <span data-ttu-id="115ea-152">Valor de cadena Unicode: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="115ea-152">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="115ea-153">Second SkipBlock</span><span class="sxs-lookup"><span data-stu-id="115ea-153">Second SkipBlock</span></span>
    
    - <span data-ttu-id="115ea-154">Tamaño: desplazamiento 0x52, 4 bytes: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="115ea-154">Size: Offset 0x52, 4 bytes: 0x0 (0).</span></span> <span data-ttu-id="115ea-155">Esta es la secuencia SkipBlock de finalización.</span><span class="sxs-lookup"><span data-stu-id="115ea-155">This is the terminating SkipBlock stream.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="115ea-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="115ea-156">See also</span></span>

- [<span data-ttu-id="115ea-157">Outlook Elementos y campos</span><span class="sxs-lookup"><span data-stu-id="115ea-157">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="115ea-158">Estructuras de secuencias</span><span class="sxs-lookup"><span data-stu-id="115ea-158">Stream Structures</span></span>](stream-structures.md)
- [<span data-ttu-id="115ea-159">Estructura de secuencia PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="115ea-159">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="115ea-160">Estructura de secuencia FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="115ea-160">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="115ea-161">Estructura de secuencias SkipBlock</span><span class="sxs-lookup"><span data-stu-id="115ea-161">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="115ea-162">Estructura de secuencias FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="115ea-162">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="115ea-163">Estructura de secuencias PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="115ea-163">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="115ea-164">Estructura de secuencias PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="115ea-164">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

