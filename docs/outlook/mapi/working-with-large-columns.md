---
title: Trabajar con columnas grandes
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
# <a name="working-with-large-columns"></a><span data-ttu-id="b977c-103">Trabajar con columnas grandes</span><span class="sxs-lookup"><span data-stu-id="b977c-103">Working with Large Columns</span></span>

  
  
<span data-ttu-id="b977c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b977c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b977c-105">Las columnas con datos de cadena o propiedad binaria pueden ser grandes, posiblemente muchos miles de bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="b977c-105">Columns with string or binary property data can be large, possibly many thousands of bytes long.</span></span> <span data-ttu-id="b977c-106">Dado que la inclusión de una o más columnas con cientos de bytes en una vista suele ser poco práctica, MAPI permite a los implementadores de tablas truncar el valor, con más frecuencia a 255 bytes y menos a 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="b977c-106">Because including one or more columns with hundreds of bytes in a view is often impractical, MAPI enables table implementers to truncate the value, most often to 255 bytes and less often to 510 bytes.</span></span> <span data-ttu-id="b977c-107">Siempre que sea posible, los implementadores de tablas deben incluir el valor completo de una propiedad en una columna de tabla.</span><span class="sxs-lookup"><span data-stu-id="b977c-107">Whenever possible, table implementers should include the full value of a property in a table column.</span></span> <span data-ttu-id="b977c-108">La alternativa recomendada es incluir solo los primeros 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="b977c-108">The recommended alternative is to include only the first 255 bytes.</span></span>
  
<span data-ttu-id="b977c-109">Los clientes no pueden saber de antemano si una tabla que están usando trunca columnas grandes.</span><span class="sxs-lookup"><span data-stu-id="b977c-109">Clients cannot know in advance whether a table they are using truncates large columns.</span></span> <span data-ttu-id="b977c-110">Deben suponer que una columna representa una propiedad truncada si la longitud de la columna es de 255 o 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="b977c-110">They should assume that a column represents a truncated property if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="b977c-111">Si es necesario, los clientes pueden recuperar directamente el valor completo de una columna truncada del objeto llamando al método [IMAPIProp::GetProps del](imapiprop-getprops.md) objeto.</span><span class="sxs-lookup"><span data-stu-id="b977c-111">If necessary, clients can directly retrieve the full value of a truncated column from the object by calling the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="b977c-112">Los clientes que están creando restricciones con propiedades grandes deben ser conscientes de que es el implementador de tabla el que debe saber cómo funcionan estas restricciones.</span><span class="sxs-lookup"><span data-stu-id="b977c-112">Clients building restrictions with large properties should be aware that it is up to the table implementer as to how these restrictions operate.</span></span> <span data-ttu-id="b977c-113">Algunos implementadores de tablas permiten que las restricciones creadas con una columna truncada se basen en el tamaño truncado, mientras que otros la basan en todo el valor.</span><span class="sxs-lookup"><span data-stu-id="b977c-113">Some table implementers allow restrictions that are built with a truncated column to be based on the truncated size while others base it on the entire value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b977c-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="b977c-114">See also</span></span>



[<span data-ttu-id="b977c-115">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="b977c-115">MAPI Tables</span></span>](mapi-tables.md)

