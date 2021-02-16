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
ms.openlocfilehash: 76d1afb750dc81b889ca8e5eb3639145c061bfc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408386"
---
# <a name="working-with-unicode-columns"></a><span data-ttu-id="eaedb-103">Trabajar con columnas Unicode</span><span class="sxs-lookup"><span data-stu-id="eaedb-103">Working with Unicode Columns</span></span>

  
  
<span data-ttu-id="eaedb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eaedb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eaedb-105">Las cadenas de caracteres de las tablas se pueden representar mediante caracteres estándar de 8 bits, que son caracteres de tipo de propiedad PT_STRING8, o caracteres Unicode de 16 bits, que son caracteres de tipo PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="eaedb-105">Character strings in tables can be represented using standard 8-bit characters, which are property type PT_STRING8, or 16-bit Unicode characters, which are property type PT_UNICODE.</span></span> <span data-ttu-id="eaedb-106">Los implementadores de tablas pueden elegir si sus tablas admiten o no cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="eaedb-106">Table implementers are free to choose whether or not their tables support Unicode strings.</span></span> <span data-ttu-id="eaedb-107">Dado que Unicode agrega valor para clientes y proveedores de servicios al ampliar el conjunto de características, se recomienda admitir Unicode siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="eaedb-107">Because Unicode adds value for both clients and service providers by extending the feature set, supporting Unicode wherever possible is recommended.</span></span> 
  
<span data-ttu-id="eaedb-108">Muchos métodos de tabla aceptan una marca que determina si se espera que los valores de propiedad de cadena sean Unicode.</span><span class="sxs-lookup"><span data-stu-id="eaedb-108">Many table methods accept a flag that dictates whether or not string property values are expected to be Unicode.</span></span> <span data-ttu-id="eaedb-109">En la entrada, especificar la marca MAPI_UNICODE indica al implementador de tabla que todos los valores de propiedad de cadena pasados con la llamada son cadenas Unicode y tienen tipos de propiedad de PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="eaedb-109">On input, specifying the MAPI_UNICODE flag indicates to the table implementer that all string property values passed in with the call are Unicode strings and have property types of PT_UNICODE.</span></span> <span data-ttu-id="eaedb-110">En el resultado, esta marca indica que todos los valores de propiedad de cadena devueltos deben ser cadenas Unicode, si es posible.</span><span class="sxs-lookup"><span data-stu-id="eaedb-110">On output, this flag indicates that all returned string property values should be Unicode strings, if possible.</span></span> <span data-ttu-id="eaedb-111">Si la marca tiene un significado para la entrada o la salida depende del método.</span><span class="sxs-lookup"><span data-stu-id="eaedb-111">Whether the flag has a meaning for input or output depends on the method.</span></span> <span data-ttu-id="eaedb-112">Los implementadores de tabla que no admiten Unicode y que se pasan MAPI_UNICODE marca devuelven el MAPI_E_BAD_CHAR_WIDTH especificado.</span><span class="sxs-lookup"><span data-stu-id="eaedb-112">Table implementers that do not support Unicode and are passed the MAPI_UNICODE flag return the MAPI_E_BAD_CHAR_WIDTH value.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eaedb-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="eaedb-113">See also</span></span>



[<span data-ttu-id="eaedb-114">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="eaedb-114">MAPI Tables</span></span>](mapi-tables.md)

