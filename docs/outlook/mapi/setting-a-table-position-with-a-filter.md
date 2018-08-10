---
title: Establecer una posición de tabla con un filtro
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4c3a5c13433fb2f037be24ddd4c877579429f7bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820646"
---
# <a name="setting-a-table-position-with-a-filter"></a><span data-ttu-id="3bcdc-103">Establecer una posición de tabla con un filtro</span><span class="sxs-lookup"><span data-stu-id="3bcdc-103">Setting a Table Position with a Filter</span></span>

  
  
<span data-ttu-id="3bcdc-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3bcdc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3bcdc-105">Los usuarios de la tabla pueden mover el cursor a una fila que coincide con un conjunto de criterios de filtro.</span><span class="sxs-lookup"><span data-stu-id="3bcdc-105">Table users can move the cursor to a row that matches a set of filter criteria.</span></span> <span data-ttu-id="3bcdc-106">Los filtros se pueden basar en una gran variedad de instrucciones, como los valores de propiedad de columna, máscaras de bits o subobjetos.</span><span class="sxs-lookup"><span data-stu-id="3bcdc-106">Filters can be based on a variety of guidelines such as column property values, bitmasks, or subobjects.</span></span> <span data-ttu-id="3bcdc-107">Los filtros se especifican en MAPI mediante una estructura de [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="3bcdc-107">Filters are specified in MAPI using an [SRestriction](srestriction.md) structure.</span></span> 
  
 <span data-ttu-id="3bcdc-108">**Para colocar una tabla a la primera fila que coincide con los criterios establecidos en una restricción**</span><span class="sxs-lookup"><span data-stu-id="3bcdc-108">**To position a table to the first row that matches the criteria established in a restriction**</span></span>
  
- <span data-ttu-id="3bcdc-109">Llame al método [IMAPITable:: FindRow](imapitable-findrow.md) .</span><span class="sxs-lookup"><span data-stu-id="3bcdc-109">Call the [IMAPITable::FindRow](imapitable-findrow.md) method.</span></span> <span data-ttu-id="3bcdc-110">A partir de la fila representada por un marcador determinado, **FindRow** busca en una dirección hacia delante o hacia atrás para localizar una fila que coincide con los criterios especificados en la restricción.</span><span class="sxs-lookup"><span data-stu-id="3bcdc-110">Starting with the row represented by a particular bookmark, **FindRow** searches in either a forward or backward direction to locate a row that matches the criteria specified in the restriction.</span></span> <span data-ttu-id="3bcdc-111">**FindRow** puede ser útil para implementar una barra de desplazamiento que se basa en las cadenas de caracteres, en lugar de valores fraccionarias.</span><span class="sxs-lookup"><span data-stu-id="3bcdc-111">**FindRow** can be useful for implementing a scroll bar that is based on character strings, instead of fractional values.</span></span> <span data-ttu-id="3bcdc-112">Por ejemplo, un cliente puede llamar a implementación de MAPI de **FindRow** cuando se realicen búsquedas a través de la libreta de direcciones integrada para permitir que un usuario, escribiendo uno o más caracteres, para buscar el nombre que comienza con los caracteres especificados.</span><span class="sxs-lookup"><span data-stu-id="3bcdc-112">For example, a client can call MAPI's implementation of **FindRow** when searching through the integrated address book to enable a user, by entering one or more characters, to locate the first name that begins with the specified characters.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3bcdc-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="3bcdc-113">See also</span></span>



[<span data-ttu-id="3bcdc-114">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="3bcdc-114">MAPI Tables</span></span>](mapi-tables.md)
