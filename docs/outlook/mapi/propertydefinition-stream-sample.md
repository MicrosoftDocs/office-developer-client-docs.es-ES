---
title: Ejemplo de secuencia de PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3d0c337bd3e5a73bbbcbb72a109320cfb84efd50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820460"
---
# <a name="propertydefinition-stream-sample"></a><span data-ttu-id="71153-103">Ejemplo de secuencia de PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="71153-103">PropertyDefinition stream sample</span></span>

<span data-ttu-id="71153-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="71153-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="71153-105">En este tema se describe un ejemplo de una secuencia de PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="71153-105">This topic describes an example of a PropertyDefinition stream.</span></span> <span data-ttu-id="71153-106">La secuencia contiene una definición de un campo definido por el usuario, `TextField1`.</span><span class="sxs-lookup"><span data-stu-id="71153-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="71153-107">El tipo es **texto**, y la definición de está en el formato PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="71153-107">The type is **Text**, and the definition is in the PropDefV2 format.</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="71153-108">Volcado de datos</span><span class="sxs-lookup"><span data-stu-id="71153-108">Data dump</span></span>

<span data-ttu-id="71153-109">El siguiente es un volcado de datos de la secuencia tal y como se mostrarían en un editor binario.</span><span class="sxs-lookup"><span data-stu-id="71153-109">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="71153-110">Desplazamiento de la secuencia</span><span class="sxs-lookup"><span data-stu-id="71153-110">Stream offset</span></span>|<span data-ttu-id="71153-111">Bytes de datos</span><span class="sxs-lookup"><span data-stu-id="71153-111">Data bytes</span></span>|<span data-ttu-id="71153-112">Datos ASCII</span><span class="sxs-lookup"><span data-stu-id="71153-112">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
<span data-ttu-id="71153-113">El siguiente es un análisis de los datos de ejemplo de la secuencia de PropertyDefinition:</span><span class="sxs-lookup"><span data-stu-id="71153-113">The following is a parse of the sample data for the PropertyDefinition stream:</span></span>
  
- <span data-ttu-id="71153-114">Versión: Desplazamiento 0 x 0, 2 bytes: 0 x 0103 (PropDefV2).</span><span class="sxs-lookup"><span data-stu-id="71153-114">Version: Offset 0x0, 2 bytes: 0x0103 (PropDefV2).</span></span>
    
- <span data-ttu-id="71153-115">FieldDefinitionCount: Desplazamiento 0 x 2, 4 bytes: 0 x 1 (1).</span><span class="sxs-lookup"><span data-stu-id="71153-115">FieldDefinitionCount: Offset 0x2, 4 bytes: 0x1 (1).</span></span>
    
- <span data-ttu-id="71153-116">FieldDefinitions: Desplazamiento 0 x 6, matriz de secuencia de FieldDefinition 1.</span><span class="sxs-lookup"><span data-stu-id="71153-116">FieldDefinitions: Offset 0x6, array of 1 FieldDefinition stream.</span></span>
    
  - <span data-ttu-id="71153-117">Indicadores: Desplazamiento 0 x 6, 4 bytes: 0 x 45 (PDO_IS_CUSTOM | PDO_PRINT_SAVEAS | PDO_PRINT_SAVEAS_DEF).</span><span class="sxs-lookup"><span data-stu-id="71153-117">Flags: Offset 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM|PDO_PRINT_SAVEAS|PDO_PRINT_SAVEAS_DEF).</span></span>
    
  - <span data-ttu-id="71153-118">VT: Desplazamiento 0xA, 2 bytes: 0 x 8 (**VT_BSTR**).</span><span class="sxs-lookup"><span data-stu-id="71153-118">VT: Offset 0xA, 2 bytes: 0x8 (**VT_BSTR**).</span></span>
    
  - <span data-ttu-id="71153-119">DispId: Desplazamiento 0xC, 4 bytes: 0 x 0 (0).</span><span class="sxs-lookup"><span data-stu-id="71153-119">DispId: Offset 0xC, 4 bytes: 0x0 (0).</span></span>
    
  - <span data-ttu-id="71153-120">NmidNameLength: Desplazamiento 0 x 10, 2 bytes: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="71153-120">NmidNameLength: Offset 0x10, 2 bytes: 0xA (10).</span></span>
    
  - <span data-ttu-id="71153-121">NmidName: Desplazamiento 0 x 12, matriz de número de 10 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="71153-121">NmidName: Offset 0x12, array of 10 WCHARs.</span></span> <span data-ttu-id="71153-122">Valor de cadena Unicode: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="71153-122">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="71153-123">NameANSI: Desplazamiento 0 x 26, PackedAnsiString secuencia.</span><span class="sxs-lookup"><span data-stu-id="71153-123">NameANSI: Offset 0x26, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="71153-124">Duración: Desplazamiento 0 x 26, 1 byte: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="71153-124">Length: Offset 0x26, 1 byte: 0xA (10).</span></span>
      
    - <span data-ttu-id="71153-125">Caracteres: Desplazamiento 0 x 27, matriz de 10 caracteres.</span><span class="sxs-lookup"><span data-stu-id="71153-125">Characters: Offset 0x27, array of 10 CHARs.</span></span> <span data-ttu-id="71153-126">Valor de cadena ANSI: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="71153-126">ANSI string value: "TextField1".</span></span>
    
  - <span data-ttu-id="71153-127">FormulaANSI: Desplazamiento 0 x 31, PackedAnsiString secuencia.</span><span class="sxs-lookup"><span data-stu-id="71153-127">FormulaANSI: Offset 0x31, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="71153-128">Duración: Desplazamiento 0 x 31, 1 byte: 0 x 0 (0).</span><span class="sxs-lookup"><span data-stu-id="71153-128">Length: Offset 0x31, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="71153-129">Caracteres: Desplazamiento 0 x 32, matriz de 0 caracteres.</span><span class="sxs-lookup"><span data-stu-id="71153-129">Characters: Offset 0x32, array of 0 CHARs.</span></span> <span data-ttu-id="71153-130">Cadena ANSI vacía.</span><span class="sxs-lookup"><span data-stu-id="71153-130">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="71153-131">ValidationRuleANSI: Desplazamiento 0 x 32, PackedAnsiString secuencia.</span><span class="sxs-lookup"><span data-stu-id="71153-131">ValidationRuleANSI: Offset 0x32, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="71153-132">Duración: Desplazamiento 0 x 32, 1 byte: 0 x 0 (0).</span><span class="sxs-lookup"><span data-stu-id="71153-132">Length: Offset 0x32, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="71153-133">Caracteres: Desplazamiento 0 x 33, matriz de 0 caracteres.</span><span class="sxs-lookup"><span data-stu-id="71153-133">Characters: Offset 0x33, array of 0 CHARs.</span></span> <span data-ttu-id="71153-134">Cadena ANSI vacía.</span><span class="sxs-lookup"><span data-stu-id="71153-134">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="71153-135">ValidationTextANSI: Desplazamiento 0 x 33, PackedAnsiString secuencia.</span><span class="sxs-lookup"><span data-stu-id="71153-135">ValidationTextANSI: Offset 0x33, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="71153-136">Duración: Desplazamiento 0 x 33, 1 byte: 0 x 0 (0).</span><span class="sxs-lookup"><span data-stu-id="71153-136">Length: Offset 0x33, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="71153-137">Caracteres: Desplazamiento 0x34, matriz de 0 caracteres.</span><span class="sxs-lookup"><span data-stu-id="71153-137">Characters: Offset 0x34, array of 0 CHARs.</span></span> <span data-ttu-id="71153-138">Cadena ANSI vacía.</span><span class="sxs-lookup"><span data-stu-id="71153-138">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="71153-139">ErrorANSI: Desplazamiento 0x34, PackedAnsiString secuencia.</span><span class="sxs-lookup"><span data-stu-id="71153-139">ErrorANSI: Offset 0x34, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="71153-140">Duración: Desplazamiento 0x34, 1 byte: 0 x 0 (0).</span><span class="sxs-lookup"><span data-stu-id="71153-140">Length: Offset 0x34, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="71153-141">Caracteres: Desplazamiento 0x35, matriz de 0 caracteres.</span><span class="sxs-lookup"><span data-stu-id="71153-141">Characters: Offset 0x35, array of 0 CHARs.</span></span> <span data-ttu-id="71153-142">Cadena ANSI vacía.</span><span class="sxs-lookup"><span data-stu-id="71153-142">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="71153-143">InternalType: Desplazamiento 0x35, 4 bytes: 0 x 0 (iTypeString).</span><span class="sxs-lookup"><span data-stu-id="71153-143">InternalType: Offset 0x35, 4 bytes: 0x0 (iTypeString).</span></span>
    
  - <span data-ttu-id="71153-144">SkipBlocks: Desplazamiento 0 x 39, serie de secuencias de SkipBlock.</span><span class="sxs-lookup"><span data-stu-id="71153-144">SkipBlocks: Offset 0x39, series of SkipBlock streams.</span></span>
    
  - <span data-ttu-id="71153-145">Primera SkipBlock</span><span class="sxs-lookup"><span data-stu-id="71153-145">First SkipBlock</span></span>
    
    - <span data-ttu-id="71153-146">Tamaño: Desplazamiento 0 x 39, 4 bytes: 0x15 (21).</span><span class="sxs-lookup"><span data-stu-id="71153-146">Size: Offset 0x39, 4 bytes: 0x15 (21).</span></span>
      
    - <span data-ttu-id="71153-147">Contenido: Desplazamiento 0x3D, matriz de bytes 21.</span><span class="sxs-lookup"><span data-stu-id="71153-147">Content: Offset 0x3D, array of 21 bytes.</span></span> <span data-ttu-id="71153-148">Esta es la primera secuencia de SkipBlock, por lo que esta matriz contiene una secuencia de FirstSkipBlockContent.</span><span class="sxs-lookup"><span data-stu-id="71153-148">This is the first SkipBlock stream, so this array contains a FirstSkipBlockContent stream.</span></span>
      
      - <span data-ttu-id="71153-149">FieldName: Desplazamiento 0x3D, PackedUnicodeString secuencia.</span><span class="sxs-lookup"><span data-stu-id="71153-149">FieldName: Offset 0x3D, PackedUnicodeString stream.</span></span>
        
        - <span data-ttu-id="71153-150">Duración: Desplazamiento 0x3D, 1 byte: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="71153-150">Length: Offset 0x3D, 1 byte: 0xA (10).</span></span>
          
        - <span data-ttu-id="71153-151">Caracteres: Desplazamiento 0x3E, matriz de número de 10 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="71153-151">Characters: Offset 0x3E, array of 10 WCHARs.</span></span> <span data-ttu-id="71153-152">Valor de cadena Unicode: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="71153-152">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="71153-153">Segundo SkipBlock</span><span class="sxs-lookup"><span data-stu-id="71153-153">Second SkipBlock</span></span>
    
    - <span data-ttu-id="71153-154">Tamaño: Desplazamiento 0 x 52, 4 bytes: 0 x 0 (0).</span><span class="sxs-lookup"><span data-stu-id="71153-154">Size: Offset 0x52, 4 bytes: 0x0 (0).</span></span> <span data-ttu-id="71153-155">Esta es la secuencia de SkipBlock terminación.</span><span class="sxs-lookup"><span data-stu-id="71153-155">This is the terminating SkipBlock stream.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71153-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="71153-156">See also</span></span>

- [<span data-ttu-id="71153-157">Campos y elementos de Outlook</span><span class="sxs-lookup"><span data-stu-id="71153-157">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="71153-158">Estructuras de secuencia</span><span class="sxs-lookup"><span data-stu-id="71153-158">Stream Structures</span></span>](stream-structures.md)
- [<span data-ttu-id="71153-159">Muestra de la secuencia PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="71153-159">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="71153-160">Muestra de la secuencia FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="71153-160">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="71153-161">Estructura de la secuencia SkipBlock</span><span class="sxs-lookup"><span data-stu-id="71153-161">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="71153-162">Estructura de la secuencia FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="71153-162">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="71153-163">Estructura de la secuencia PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="71153-163">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="71153-164">Estructura de la secuencia PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="71153-164">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

