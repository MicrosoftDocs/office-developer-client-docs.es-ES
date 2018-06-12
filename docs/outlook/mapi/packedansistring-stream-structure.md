---
title: Estructura de la secuencia de PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 5494558db65e19891848264c170ba85a55c5df71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818461"
---
# <a name="packedansistring-stream-structure"></a><span data-ttu-id="dfd9a-103">Estructura de la secuencia de PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="dfd9a-103">PackedAnsiString Stream Structure</span></span>

  
  
<span data-ttu-id="dfd9a-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dfd9a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dfd9a-105">La estructura de la secuencia de PackedAnsiString contiene una representación ANSI de una cadena, en función de la página de códigos ANSI del equipo donde se ejecuta Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="dfd9a-105">The PackedAnsiString stream structure contains an ANSI representation of a string, based on the ANSI code page of the computer on which Microsoft Outlook is running.</span></span> <span data-ttu-id="dfd9a-106">Esta cadena no termina con un carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="dfd9a-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="dfd9a-107">Elementos de datos en esta secuencia se almacenan en orden de bytes little-endian, inmediatamente después de entre sí en el orden indicado a continuación.</span><span class="sxs-lookup"><span data-stu-id="dfd9a-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="dfd9a-108">Los elementos de datos reales que existen dependen de la longitud de la cadena de representación ANSI.</span><span class="sxs-lookup"><span data-stu-id="dfd9a-108">The actual data elements that exist depend on the length of the string in ANSI representation.</span></span>
  
- <span data-ttu-id="dfd9a-109">Una cadena cuya representación ANSI contiene menos de 255 bytes, los elementos de datos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="dfd9a-109">For a string whose ANSI representation contains less than 255 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="dfd9a-110">Duración: Bytes (1 byte), la longitud, en número de bytes, de la representación ANSI de la cadena.</span><span class="sxs-lookup"><span data-stu-id="dfd9a-110">Length: BYTE (1 byte), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="dfd9a-111">Caracteres: Una matriz de CHAR.</span><span class="sxs-lookup"><span data-stu-id="dfd9a-111">Characters: An array of CHAR.</span></span> <span data-ttu-id="dfd9a-112">El recuento de esta matriz es igual al elemento de datos de longitud.</span><span class="sxs-lookup"><span data-stu-id="dfd9a-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="dfd9a-113">Los datos de la matriz están la representación ANSI de la cadena.</span><span class="sxs-lookup"><span data-stu-id="dfd9a-113">The data in the array is the ANSI representation of the string.</span></span>
    
- <span data-ttu-id="dfd9a-114">Una cadena cuya representación ANSI contiene 255 a 65535 bytes, los elementos de datos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="dfd9a-114">For a string whose ANSI representation contains 255 to 65535 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="dfd9a-115">Prefijo: Bytes (1 byte), el valor de 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="dfd9a-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="dfd9a-116">Duración: WORD (2 bytes), la longitud, en número de bytes, de la representación ANSI de la cadena.</span><span class="sxs-lookup"><span data-stu-id="dfd9a-116">Length: WORD (2 bytes), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="dfd9a-117">Caracteres: Una matriz de CHAR.</span><span class="sxs-lookup"><span data-stu-id="dfd9a-117">Characters: An array of CHAR.</span></span> <span data-ttu-id="dfd9a-118">El recuento de esta matriz es igual al elemento de datos de longitud.</span><span class="sxs-lookup"><span data-stu-id="dfd9a-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="dfd9a-119">Los datos de la matriz están la representación ANSI de la cadena.</span><span class="sxs-lookup"><span data-stu-id="dfd9a-119">The data in the array is the ANSI representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dfd9a-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="dfd9a-120">See also</span></span>



[<span data-ttu-id="dfd9a-121">Campos y elementos de outlook</span><span class="sxs-lookup"><span data-stu-id="dfd9a-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="dfd9a-122">Estructuras de secuencia</span><span class="sxs-lookup"><span data-stu-id="dfd9a-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="dfd9a-123">Estructura de secuencia FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="dfd9a-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

