---
title: Trabajar con columnas Unicode
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9f1fd2d4e4bfdc9ccbbb771fedf1141769c8c8ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820975"
---
# <a name="working-with-unicode-columns"></a><span data-ttu-id="93c7b-103">Trabajar con columnas Unicode</span><span class="sxs-lookup"><span data-stu-id="93c7b-103">Working with Unicode Columns</span></span>

  
  
<span data-ttu-id="93c7b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="93c7b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="93c7b-105">Las cadenas de caracteres en las tablas se pueden representar mediante caracteres de 8 bits estándar, que son el tipo de propiedad PT_STRING8, o caracteres Unicode de 16 bits, que son propiedad de tipo PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="93c7b-105">Character strings in tables can be represented using standard 8-bit characters, which are property type PT_STRING8, or 16-bit Unicode characters, which are property type PT_UNICODE.</span></span> <span data-ttu-id="93c7b-106">Los implementadores de tabla son libres de elegir si sus tablas admiten cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="93c7b-106">Table implementers are free to choose whether or not their tables support Unicode strings.</span></span> <span data-ttu-id="93c7b-107">Como Unicode agrega valor para los clientes y proveedores de servicios de ampliando el conjunto de características, se recomienda la compatibilidad con Unicode siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="93c7b-107">Because Unicode adds value for both clients and service providers by extending the feature set, supporting Unicode wherever possible is recommended.</span></span> 
  
<span data-ttu-id="93c7b-108">Muchos métodos de tabla aceptan una marca que determina si los valores de propiedad de cadena se prevé que Unicode.</span><span class="sxs-lookup"><span data-stu-id="93c7b-108">Many table methods accept a flag that dictates whether or not string property values are expected to be Unicode.</span></span> <span data-ttu-id="93c7b-109">En la entrada, si se especifica el indicador MAPI_UNICODE indica para el implementador de tabla que todos los valores de propiedad de cadena pasados con la llamada son cadenas Unicode y tienen tipos de propiedad de PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="93c7b-109">On input, specifying the MAPI_UNICODE flag indicates to the table implementer that all string property values passed in with the call are Unicode strings and have property types of PT_UNICODE.</span></span> <span data-ttu-id="93c7b-110">En la salida, esta marca indica que todos los valores de propiedad de la cadena devuelta deben ser cadenas Unicode, si es posible.</span><span class="sxs-lookup"><span data-stu-id="93c7b-110">On output, this flag indicates that all returned string property values should be Unicode strings, if possible.</span></span> <span data-ttu-id="93c7b-111">Si el marcador no tiene un significado para la entrada o salida depende del método.</span><span class="sxs-lookup"><span data-stu-id="93c7b-111">Whether the flag has a meaning for input or output depends on the method.</span></span> <span data-ttu-id="93c7b-112">Los implementadores de tabla que no admiten Unicode y se pasan el indicador MAPI_UNICODE devolver el valor MAPI_E_BAD_CHAR_WIDTH.</span><span class="sxs-lookup"><span data-stu-id="93c7b-112">Table implementers that do not support Unicode and are passed the MAPI_UNICODE flag return the MAPI_E_BAD_CHAR_WIDTH value.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="93c7b-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="93c7b-113">See also</span></span>



[<span data-ttu-id="93c7b-114">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="93c7b-114">MAPI Tables</span></span>](mapi-tables.md)

