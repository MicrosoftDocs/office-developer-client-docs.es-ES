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
ms.openlocfilehash: a191a8551d425d7e8b3b9a281936a4a0e2dfd587
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820974"
---
# <a name="working-with-large-columns"></a><span data-ttu-id="2224b-103">Trabajar con columnas de gran tamaño</span><span class="sxs-lookup"><span data-stu-id="2224b-103">Working with Large Columns</span></span>

  
  
<span data-ttu-id="2224b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2224b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2224b-105">Columnas con datos de propiedad de cadena o binario pueden ser grandes, posiblemente varios miles de bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="2224b-105">Columns with string or binary property data can be large, possibly many thousands of bytes long.</span></span> <span data-ttu-id="2224b-106">Debido a que a menudo es práctico incluir una o varias columnas con cientos de bytes en una vista, MAPI permite a los implementadores de tabla truncar el valor, con más frecuencia a 255 bytes y con menos frecuencia a 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="2224b-106">Because including one or more columns with hundreds of bytes in a view is often impractical, MAPI enables table implementers to truncate the value, most often to 255 bytes and less often to 510 bytes.</span></span> <span data-ttu-id="2224b-107">Siempre que sea posible, los implementadores de tabla deben incluir el valor completo de una propiedad en una columna de tabla.</span><span class="sxs-lookup"><span data-stu-id="2224b-107">Whenever possible, table implementers should include the full value of a property in a table column.</span></span> <span data-ttu-id="2224b-108">La alternativa recomendada es incluir sólo los primeros 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="2224b-108">The recommended alternative is to include only the first 255 bytes.</span></span>
  
<span data-ttu-id="2224b-109">Los clientes no se pueden saber de antemano si una tabla que utilicen trunca columnas de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="2224b-109">Clients cannot know in advance whether a table they are using truncates large columns.</span></span> <span data-ttu-id="2224b-110">Debe asumir que una columna representa una propiedad truncada si la longitud de la columna es de 255 o 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="2224b-110">They should assume that a column represents a truncated property if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="2224b-111">Si es necesario, los clientes pueden recuperar directamente el valor completo de una columna truncada desde el objeto llamando al método del objeto [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="2224b-111">If necessary, clients can directly retrieve the full value of a truncated column from the object by calling the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="2224b-112">Creación de restricciones con propiedades de gran tamaño de los clientes deben tener en cuenta que es responsabilidad del implementador de tabla sobre cómo estas restricciones operar.</span><span class="sxs-lookup"><span data-stu-id="2224b-112">Clients building restrictions with large properties should be aware that it is up to the table implementer as to how these restrictions operate.</span></span> <span data-ttu-id="2224b-113">Algunos implementadores tabla permiten las restricciones que se crean con una columna truncada a ser según el tamaño truncado mientras que otros usuarios basar en el valor completo.</span><span class="sxs-lookup"><span data-stu-id="2224b-113">Some table implementers allow restrictions that are built with a truncated column to be based on the truncated size while others base it on the entire value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2224b-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="2224b-114">See also</span></span>



[<span data-ttu-id="2224b-115">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="2224b-115">MAPI Tables</span></span>](mapi-tables.md)

