---
title: Estructura de la secuencia PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 00791ab47cc3c6bd435d6f581e5ada53ae59d73b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569200"
---
# <a name="packedunicodestring-stream-structure"></a><span data-ttu-id="99cfd-103">Estructura de la secuencia PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="99cfd-103">PackedUnicodeString Stream Structure</span></span>

  
  
<span data-ttu-id="99cfd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99cfd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99cfd-105">La estructura de la secuencia de PackedUnicodeString contiene una representación Unicode (UTF-16) de una cadena.</span><span class="sxs-lookup"><span data-stu-id="99cfd-105">The PackedUnicodeString stream structure contains a Unicode (UTF-16) representation of a string.</span></span> <span data-ttu-id="99cfd-106">Esta cadena no termina con un carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="99cfd-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="99cfd-107">Elementos de datos en esta secuencia se almacenan en orden de bytes little-endian, inmediatamente después de entre sí en el orden indicado a continuación.</span><span class="sxs-lookup"><span data-stu-id="99cfd-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="99cfd-108">Los elementos de datos reales que existen dependen de la longitud de la cadena de representación UTF-16.</span><span class="sxs-lookup"><span data-stu-id="99cfd-108">The actual data elements that exist depend on the length of the string in UTF-16 representation.</span></span>
  
- <span data-ttu-id="99cfd-109">Una cadena cuya representación UTF-16 contiene el número de WCHAR menor que 255, los elementos de datos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="99cfd-109">For a string whose UTF-16 representation contains less than 255 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="99cfd-110">Duración: Bytes (1 byte), la longitud, en número de número de WCHAR, de la representación UTF-16 de la cadena.</span><span class="sxs-lookup"><span data-stu-id="99cfd-110">Length: BYTE (1 byte), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="99cfd-111">Caracteres: Una matriz de WCHAR.</span><span class="sxs-lookup"><span data-stu-id="99cfd-111">Characters: An array of WCHAR.</span></span> <span data-ttu-id="99cfd-112">El recuento de esta matriz es igual al elemento de datos de longitud.</span><span class="sxs-lookup"><span data-stu-id="99cfd-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="99cfd-113">Los datos de la matriz están la representación UTF-16 de la cadena.</span><span class="sxs-lookup"><span data-stu-id="99cfd-113">The data in the array is the UTF-16 representation of the string.</span></span>
    
- <span data-ttu-id="99cfd-114">Una cadena cuya representación UTF-16 contiene el número de 255 a 65535 WCHAR, los elementos de datos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="99cfd-114">For a string whose UTF-16 representation contains 255 to 65535 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="99cfd-115">Prefijo: Bytes (1 byte), el valor de 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="99cfd-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="99cfd-116">Duración: WORD (2 bytes), la longitud, en número de número de WCHAR, de la representación UTF-16 de la cadena.</span><span class="sxs-lookup"><span data-stu-id="99cfd-116">Length: WORD (2 bytes), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="99cfd-117">Caracteres: Una matriz de WCHAR.</span><span class="sxs-lookup"><span data-stu-id="99cfd-117">Characters: An array of WCHAR.</span></span> <span data-ttu-id="99cfd-118">El recuento de esta matriz es igual al elemento de datos de longitud.</span><span class="sxs-lookup"><span data-stu-id="99cfd-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="99cfd-119">Los datos de la matriz están la representación UTF-16 de la cadena.</span><span class="sxs-lookup"><span data-stu-id="99cfd-119">The data in the array is the UTF-16 representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="99cfd-120">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="99cfd-120">See also</span></span>



[<span data-ttu-id="99cfd-121">Campos y elementos de Outlook</span><span class="sxs-lookup"><span data-stu-id="99cfd-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="99cfd-122">Estructuras de secuencia</span><span class="sxs-lookup"><span data-stu-id="99cfd-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="99cfd-123">Muestra de la secuencia FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="99cfd-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

