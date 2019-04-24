---
title: Estructura de la secuencia PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348513"
---
# <a name="packedansistring-stream-structure"></a><span data-ttu-id="bd73f-103">Estructura de la secuencia PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="bd73f-103">PackedAnsiString Stream Structure</span></span>

  
  
<span data-ttu-id="bd73f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd73f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd73f-105">La estructura de la secuencia PackedAnsiString contiene una representación ANSI de una cadena, basada en la página de códigos ANSI del equipo en el que se está ejecutando Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="bd73f-105">The PackedAnsiString stream structure contains an ANSI representation of a string, based on the ANSI code page of the computer on which Microsoft Outlook is running.</span></span> <span data-ttu-id="bd73f-106">Esta cadena no termina con un carácter null.</span><span class="sxs-lookup"><span data-stu-id="bd73f-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="bd73f-107">Los elementos de datos de esta secuencia se almacenan en el orden de bytes Little-endian, inmediatamente a continuación entre sí en el orden indicado a continuación.</span><span class="sxs-lookup"><span data-stu-id="bd73f-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="bd73f-108">Los elementos de datos reales que existen dependen de la longitud de la cadena en la representación ANSI.</span><span class="sxs-lookup"><span data-stu-id="bd73f-108">The actual data elements that exist depend on the length of the string in ANSI representation.</span></span>
  
- <span data-ttu-id="bd73f-109">En el caso de una cadena cuya representación ANSI contenga menos de 255 bytes, los elementos de datos serán los siguientes:</span><span class="sxs-lookup"><span data-stu-id="bd73f-109">For a string whose ANSI representation contains less than 255 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="bd73f-110">Longitud: BYTE (1 byte), longitud, en número de bytes, de la representación ANSI de la cadena.</span><span class="sxs-lookup"><span data-stu-id="bd73f-110">Length: BYTE (1 byte), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="bd73f-111">Caracteres: una matriz de CHAR.</span><span class="sxs-lookup"><span data-stu-id="bd73f-111">Characters: An array of CHAR.</span></span> <span data-ttu-id="bd73f-112">El recuento de esta matriz es igual al elemento de datos de longitud.</span><span class="sxs-lookup"><span data-stu-id="bd73f-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="bd73f-113">Los datos de la matriz son la representación ANSI de la cadena.</span><span class="sxs-lookup"><span data-stu-id="bd73f-113">The data in the array is the ANSI representation of the string.</span></span>
    
- <span data-ttu-id="bd73f-114">Para una cadena cuya representación ANSI contiene de 255 a 65535 bytes, los elementos de datos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="bd73f-114">For a string whose ANSI representation contains 255 to 65535 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="bd73f-115">Prefix: BYTE (1 byte), el valor de 255 (0xFF).</span><span class="sxs-lookup"><span data-stu-id="bd73f-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="bd73f-116">Longitud: WORD (2 bytes), la longitud, en número de bytes, de la representación ANSI de la cadena.</span><span class="sxs-lookup"><span data-stu-id="bd73f-116">Length: WORD (2 bytes), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="bd73f-117">Caracteres: una matriz de CHAR.</span><span class="sxs-lookup"><span data-stu-id="bd73f-117">Characters: An array of CHAR.</span></span> <span data-ttu-id="bd73f-118">El recuento de esta matriz es igual al elemento de datos de longitud.</span><span class="sxs-lookup"><span data-stu-id="bd73f-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="bd73f-119">Los datos de la matriz son la representación ANSI de la cadena.</span><span class="sxs-lookup"><span data-stu-id="bd73f-119">The data in the array is the ANSI representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd73f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd73f-120">See also</span></span>



[<span data-ttu-id="bd73f-121">Campos y elementos de Outlook</span><span class="sxs-lookup"><span data-stu-id="bd73f-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="bd73f-122">Estructuras de secuencia</span><span class="sxs-lookup"><span data-stu-id="bd73f-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="bd73f-123">Estructura de la secuencia FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="bd73f-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

