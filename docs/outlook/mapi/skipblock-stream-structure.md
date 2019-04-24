---
title: Estructura de la secuencia SkipBlock
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5a3367a15374234658fd9d10f3c2a5f3a191c80e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282673"
---
# <a name="skipblock-stream-structure"></a><span data-ttu-id="6f28c-103">Estructura de la secuencia SkipBlock</span><span class="sxs-lookup"><span data-stu-id="6f28c-103">SkipBlock Stream Structure</span></span>

  
  
<span data-ttu-id="6f28c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f28c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f28c-105">Una estructura de secuencia SkipBlock es un bloque de datos que comienza con un entero que especifica la longitud de la parte restante del bloque.</span><span class="sxs-lookup"><span data-stu-id="6f28c-105">A SkipBlock stream structure is a block of data that starts with an integer that specifies the length of the remaining part of the block.</span></span> <span data-ttu-id="6f28c-106">Esta estructura de secuencia existe en una secuencia [FieldDefinition](fielddefinition-stream-structure.md) si la definición del campo está en formato PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="6f28c-106">This stream structure exists in a [FieldDefinition](fielddefinition-stream-structure.md) stream if the field definition is in PropDefV2 format.</span></span> 
  
<span data-ttu-id="6f28c-107">El propósito de una estructura de secuencia SkipBlock depende de su ubicación relativa en una serie de estructuras like en el elemento de datos SkipBlocks de una secuencia FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="6f28c-107">The purpose of a SkipBlock stream structure depends on its relative location in a series of like structures in the SkipBlocks data element of a FieldDefinition stream.</span></span> <span data-ttu-id="6f28c-108">La serie SkipBlocks debe contener al menos una estructura SkipBlock que finalice la serie y tenga el elemento de datos tamaño igual a 0.</span><span class="sxs-lookup"><span data-stu-id="6f28c-108">The SkipBlocks series should contain at least one SkipBlock structure that terminates the series and has the Size data element equal to 0.</span></span> <span data-ttu-id="6f28c-109">Si la primera estructura no es la estructura final (es decir, el elemento de datos size es mayor que 0), Outlook supone que la primera estructura especifica el nombre del campo en Unicode (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="6f28c-109">If the first structure is not the terminating structure (that is, the Size data element is greater than 0), Outlook assumes the first structure specifies the field name in Unicode (UTF-16).</span></span>
  
<span data-ttu-id="6f28c-110">Los elementos de datos de esta secuencia se almacenan en el orden de bytes Little-endian, inmediatamente a continuación entre sí en el orden especificado a continuación.</span><span class="sxs-lookup"><span data-stu-id="6f28c-110">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="6f28c-111">Size: DWORD (4 bytes), el tamaño, en número de bytes, del elemento de datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="6f28c-111">Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.</span></span>
    
- <span data-ttu-id="6f28c-112">Content: una matriz de BYTEs.</span><span class="sxs-lookup"><span data-stu-id="6f28c-112">Content: An array of BYTE.</span></span> <span data-ttu-id="6f28c-113">El recuento de esta matriz es igual al elemento de datos de tamaño.</span><span class="sxs-lookup"><span data-stu-id="6f28c-113">The count of this array is equal to the Size data element.</span></span> <span data-ttu-id="6f28c-114">El significado del elemento de datos de contenido depende de la ubicación de la estructura SkipBlock en la serie y la versión de Outlook.</span><span class="sxs-lookup"><span data-stu-id="6f28c-114">The meaning of the Content data element depends on the location of the SkipBlock structure in the series and the version of Outlook.</span></span> <span data-ttu-id="6f28c-115">Si la primera estructura SkipBlock no es la estructura de terminación, Outlook considera la primera estructura SkipBlock como la estructura de la secuencia [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) que especifica el nombre del campo en Unicode.</span><span class="sxs-lookup"><span data-stu-id="6f28c-115">If the first SkipBlock structure is not the terminating structure, Outlook considers the first SkipBlock structure as the [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) stream structure that specifies the field name in Unicode.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6f28c-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f28c-116">See also</span></span>



[<span data-ttu-id="6f28c-117">Campos y elementos de Outlook</span><span class="sxs-lookup"><span data-stu-id="6f28c-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="6f28c-118">Estructuras de secuencia</span><span class="sxs-lookup"><span data-stu-id="6f28c-118">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="6f28c-119">Estructura de la secuencia FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="6f28c-119">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="6f28c-120">Estructura de la secuencia FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="6f28c-120">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)

