---
title: Estructura de secuencias PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404508"
---
# <a name="packedansistring-stream-structure"></a><span data-ttu-id="56c16-103">Estructura de secuencias PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="56c16-103">PackedAnsiString Stream Structure</span></span>

  
  
<span data-ttu-id="56c16-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56c16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56c16-105">La estructura de secuencia PackedAnsiString contiene una representación ANSI de una cadena, basada en la página de código ANSI del equipo en el que se ejecuta Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="56c16-105">The PackedAnsiString stream structure contains an ANSI representation of a string, based on the ANSI code page of the computer on which Microsoft Outlook is running.</span></span> <span data-ttu-id="56c16-106">Esta cadena no termina con un carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="56c16-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="56c16-107">Los elementos de datos de esta secuencia se almacenan en orden de bytes little-endian, siguiendo inmediatamente entre sí en el orden que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="56c16-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="56c16-108">Los elementos de datos reales que existen dependen de la longitud de la cadena en la representación ANSI.</span><span class="sxs-lookup"><span data-stu-id="56c16-108">The actual data elements that exist depend on the length of the string in ANSI representation.</span></span>
  
- <span data-ttu-id="56c16-109">Para una cadena cuya representación ANSI contiene menos de 255 bytes, los elementos de datos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="56c16-109">For a string whose ANSI representation contains less than 255 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="56c16-110">Length: BYTE (1 byte), la longitud, en número de bytes, de la representación ANSI de la cadena.</span><span class="sxs-lookup"><span data-stu-id="56c16-110">Length: BYTE (1 byte), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="56c16-111">Caracteres: una matriz de CHAR.</span><span class="sxs-lookup"><span data-stu-id="56c16-111">Characters: An array of CHAR.</span></span> <span data-ttu-id="56c16-112">El recuento de esta matriz es igual al elemento de datos Length.</span><span class="sxs-lookup"><span data-stu-id="56c16-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="56c16-113">Los datos de la matriz son la representación ANSI de la cadena.</span><span class="sxs-lookup"><span data-stu-id="56c16-113">The data in the array is the ANSI representation of the string.</span></span>
    
- <span data-ttu-id="56c16-114">Para una cadena cuya representación ANSI contiene de 255 a 65535 bytes, los elementos de datos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="56c16-114">For a string whose ANSI representation contains 255 to 65535 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="56c16-115">Prefijo: BYTE (1 byte), el valor de 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="56c16-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="56c16-116">Length: WORD (2 bytes), la longitud, en número de bytes, de la representación ANSI de la cadena.</span><span class="sxs-lookup"><span data-stu-id="56c16-116">Length: WORD (2 bytes), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="56c16-117">Caracteres: una matriz de CHAR.</span><span class="sxs-lookup"><span data-stu-id="56c16-117">Characters: An array of CHAR.</span></span> <span data-ttu-id="56c16-118">El recuento de esta matriz es igual al elemento de datos Length.</span><span class="sxs-lookup"><span data-stu-id="56c16-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="56c16-119">Los datos de la matriz son la representación ANSI de la cadena.</span><span class="sxs-lookup"><span data-stu-id="56c16-119">The data in the array is the ANSI representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56c16-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="56c16-120">See also</span></span>



[<span data-ttu-id="56c16-121">Outlook Elementos y campos</span><span class="sxs-lookup"><span data-stu-id="56c16-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="56c16-122">Estructuras de secuencias</span><span class="sxs-lookup"><span data-stu-id="56c16-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="56c16-123">Estructura de secuencia FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="56c16-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

