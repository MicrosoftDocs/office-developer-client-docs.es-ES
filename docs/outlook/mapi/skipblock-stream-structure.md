---
title: Estructura de la secuencia SkipBlock
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b7be498473ef86b11006702f85089f0f95bb2e37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580904"
---
# <a name="skipblock-stream-structure"></a><span data-ttu-id="66524-103">Estructura de la secuencia SkipBlock</span><span class="sxs-lookup"><span data-stu-id="66524-103">SkipBlock Stream Structure</span></span>

  
  
<span data-ttu-id="66524-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66524-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66524-105">Una estructura de secuencia de SkipBlock es un bloque de datos que comienza con un número entero que especifica la longitud de la parte restante del bloque.</span><span class="sxs-lookup"><span data-stu-id="66524-105">A SkipBlock stream structure is a block of data that starts with an integer that specifies the length of the remaining part of the block.</span></span> <span data-ttu-id="66524-106">Esta estructura de secuencia existe en una secuencia [FieldDefinition](fielddefinition-stream-structure.md) si la definición de campo se encuentra en formato de PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="66524-106">This stream structure exists in a [FieldDefinition](fielddefinition-stream-structure.md) stream if the field definition is in PropDefV2 format.</span></span> 
  
<span data-ttu-id="66524-107">El propósito de una estructura de secuencia SkipBlock depende de la ubicación relativa en una serie de como estructuras en el elemento de datos de SkipBlocks de una secuencia FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="66524-107">The purpose of a SkipBlock stream structure depends on its relative location in a series of like structures in the SkipBlocks data element of a FieldDefinition stream.</span></span> <span data-ttu-id="66524-108">La serie SkipBlocks debe contener al menos una estructura SkipBlock que finaliza la serie y que tenga el elemento de datos de tamaño igual a 0.</span><span class="sxs-lookup"><span data-stu-id="66524-108">The SkipBlocks series should contain at least one SkipBlock structure that terminates the series and has the Size data element equal to 0.</span></span> <span data-ttu-id="66524-109">Si la primera estructura no es la estructura de terminación (es decir, el elemento de datos de tamaño es mayor que 0), Outlook se da por supuesto que la primera estructura especifica el nombre del campo en Unicode (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="66524-109">If the first structure is not the terminating structure (that is, the Size data element is greater than 0), Outlook assumes the first structure specifies the field name in Unicode (UTF-16).</span></span>
  
<span data-ttu-id="66524-110">Elementos de datos en esta secuencia se almacenan en orden de bytes little-endian, inmediatamente después de entre sí en el orden especificado a continuación.</span><span class="sxs-lookup"><span data-stu-id="66524-110">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="66524-111">Tamaño: DWORD (4 bytes), el tamaño, en número de bytes, del elemento de datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="66524-111">Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.</span></span>
    
- <span data-ttu-id="66524-112">Contenido: Una matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="66524-112">Content: An array of BYTE.</span></span> <span data-ttu-id="66524-113">El recuento de esta matriz es igual al elemento de datos de tamaño.</span><span class="sxs-lookup"><span data-stu-id="66524-113">The count of this array is equal to the Size data element.</span></span> <span data-ttu-id="66524-114">El significado del elemento de datos de contenido depende de la ubicación de la estructura de SkipBlock en la serie y la versión de Outlook.</span><span class="sxs-lookup"><span data-stu-id="66524-114">The meaning of the Content data element depends on the location of the SkipBlock structure in the series and the version of Outlook.</span></span> <span data-ttu-id="66524-115">Si la primera estructura SkipBlock no es la estructura de terminación, Outlook considera la primera estructura SkipBlock como la estructura de la secuencia de [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) que especifica el nombre del campo en Unicode.</span><span class="sxs-lookup"><span data-stu-id="66524-115">If the first SkipBlock structure is not the terminating structure, Outlook considers the first SkipBlock structure as the [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) stream structure that specifies the field name in Unicode.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="66524-116">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="66524-116">See also</span></span>



[<span data-ttu-id="66524-117">Campos y elementos de Outlook</span><span class="sxs-lookup"><span data-stu-id="66524-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="66524-118">Estructuras de secuencia</span><span class="sxs-lookup"><span data-stu-id="66524-118">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="66524-119">Muestra de la secuencia FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="66524-119">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="66524-120">Estructura de la secuencia FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="66524-120">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)

