---
title: Trabajar con columnas de gran tamaño
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9ca3c5e7a0d1b4a6ac09dcfcc7db10ec76ecb224
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420426"
---
# <a name="working-with-large-columns"></a><span data-ttu-id="927e6-103">Trabajar con columnas de gran tamaño</span><span class="sxs-lookup"><span data-stu-id="927e6-103">Working with Large Columns</span></span>

  
  
<span data-ttu-id="927e6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="927e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="927e6-105">Las columnas con datos de String o Binary Property pueden ser grandes, posiblemente miles de bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="927e6-105">Columns with string or binary property data can be large, possibly many thousands of bytes long.</span></span> <span data-ttu-id="927e6-106">Debido a que la inclusión de una o más columnas con cientos de bytes en una vista es a menudo inviable, MAPI permite que los implementadores de tablas trunquen el valor, con mayor frecuencia a 255 bytes y menos frecuencia a 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="927e6-106">Because including one or more columns with hundreds of bytes in a view is often impractical, MAPI enables table implementers to truncate the value, most often to 255 bytes and less often to 510 bytes.</span></span> <span data-ttu-id="927e6-107">Siempre que sea posible, los implementadores de tablas deben incluir el valor completo de una propiedad en una columna de tabla.</span><span class="sxs-lookup"><span data-stu-id="927e6-107">Whenever possible, table implementers should include the full value of a property in a table column.</span></span> <span data-ttu-id="927e6-108">La alternativa recomendada es incluir solo los primeros 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="927e6-108">The recommended alternative is to include only the first 255 bytes.</span></span>
  
<span data-ttu-id="927e6-109">Los clientes no pueden saber de antemano si una tabla que usan trunca columnas de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="927e6-109">Clients cannot know in advance whether a table they are using truncates large columns.</span></span> <span data-ttu-id="927e6-110">Deben dar por hecho que una columna representa una propiedad truncada si la longitud de la columna es de 255 o de 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="927e6-110">They should assume that a column represents a truncated property if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="927e6-111">Si es necesario, los clientes pueden recuperar directamente el valor completo de una columna truncada del objeto llamando al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del objeto.</span><span class="sxs-lookup"><span data-stu-id="927e6-111">If necessary, clients can directly retrieve the full value of a truncated column from the object by calling the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="927e6-112">Los clientes que crean restricciones con propiedades grandes deben tener en cuenta que es el que implementa la tabla en cuanto al funcionamiento de estas restricciones.</span><span class="sxs-lookup"><span data-stu-id="927e6-112">Clients building restrictions with large properties should be aware that it is up to the table implementer as to how these restrictions operate.</span></span> <span data-ttu-id="927e6-113">Algunos implementadores de tablas permiten restricciones que se generan con una columna truncada para basarse en el tamaño truncado mientras que otros basan en el valor completo.</span><span class="sxs-lookup"><span data-stu-id="927e6-113">Some table implementers allow restrictions that are built with a truncated column to be based on the truncated size while others base it on the entire value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="927e6-114">Ver también</span><span class="sxs-lookup"><span data-stu-id="927e6-114">See also</span></span>



[<span data-ttu-id="927e6-115">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="927e6-115">MAPI Tables</span></span>](mapi-tables.md)

