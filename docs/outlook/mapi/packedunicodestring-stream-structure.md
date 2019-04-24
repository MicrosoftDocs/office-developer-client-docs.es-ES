---
title: Estructura de la secuencia PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fc20c259f30ded2f96f3bf314e74207bebcac980
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348478"
---
# <a name="packedunicodestring-stream-structure"></a><span data-ttu-id="38be8-103">Estructura de la secuencia PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="38be8-103">PackedUnicodeString Stream Structure</span></span>

  
  
<span data-ttu-id="38be8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38be8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38be8-105">La estructura de la secuencia PackedUnicodeString contiene una representación Unicode (UTF-16) de una cadena.</span><span class="sxs-lookup"><span data-stu-id="38be8-105">The PackedUnicodeString stream structure contains a Unicode (UTF-16) representation of a string.</span></span> <span data-ttu-id="38be8-106">Esta cadena no termina con un carácter null.</span><span class="sxs-lookup"><span data-stu-id="38be8-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="38be8-107">Los elementos de datos de esta secuencia se almacenan en el orden de bytes Little-endian, inmediatamente a continuación entre sí en el orden indicado a continuación.</span><span class="sxs-lookup"><span data-stu-id="38be8-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="38be8-108">Los elementos de datos reales que existen dependen de la longitud de la cadena en la representación UTF-16.</span><span class="sxs-lookup"><span data-stu-id="38be8-108">The actual data elements that exist depend on the length of the string in UTF-16 representation.</span></span>
  
- <span data-ttu-id="38be8-109">Para una cadena cuya representación UTF-16 contiene menos de 255 WCHARs, los elementos de datos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="38be8-109">For a string whose UTF-16 representation contains less than 255 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="38be8-110">Longitud: BYTE (1 byte), longitud, en número de WCHARs, de la representación UTF-16 de la cadena.</span><span class="sxs-lookup"><span data-stu-id="38be8-110">Length: BYTE (1 byte), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="38be8-111">Caracteres: una matriz de WCHAR.</span><span class="sxs-lookup"><span data-stu-id="38be8-111">Characters: An array of WCHAR.</span></span> <span data-ttu-id="38be8-112">El recuento de esta matriz es igual al elemento de datos de longitud.</span><span class="sxs-lookup"><span data-stu-id="38be8-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="38be8-113">Los datos de la matriz son la representación UTF-16 de la cadena.</span><span class="sxs-lookup"><span data-stu-id="38be8-113">The data in the array is the UTF-16 representation of the string.</span></span>
    
- <span data-ttu-id="38be8-114">Para una cadena cuya representación UTF-16 contiene de 255 a 65535 WCHARs, los elementos de datos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="38be8-114">For a string whose UTF-16 representation contains 255 to 65535 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="38be8-115">Prefix: BYTE (1 byte), el valor de 255 (0xFF).</span><span class="sxs-lookup"><span data-stu-id="38be8-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="38be8-116">Longitud: WORD (2 bytes), la longitud, en número de WCHARs, de la representación UTF-16 de la cadena.</span><span class="sxs-lookup"><span data-stu-id="38be8-116">Length: WORD (2 bytes), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="38be8-117">Caracteres: una matriz de WCHAR.</span><span class="sxs-lookup"><span data-stu-id="38be8-117">Characters: An array of WCHAR.</span></span> <span data-ttu-id="38be8-118">El recuento de esta matriz es igual al elemento de datos de longitud.</span><span class="sxs-lookup"><span data-stu-id="38be8-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="38be8-119">Los datos de la matriz son la representación UTF-16 de la cadena.</span><span class="sxs-lookup"><span data-stu-id="38be8-119">The data in the array is the UTF-16 representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38be8-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="38be8-120">See also</span></span>



[<span data-ttu-id="38be8-121">Campos y elementos de Outlook</span><span class="sxs-lookup"><span data-stu-id="38be8-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="38be8-122">Estructuras de secuencia</span><span class="sxs-lookup"><span data-stu-id="38be8-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="38be8-123">Estructura de la secuencia FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="38be8-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

