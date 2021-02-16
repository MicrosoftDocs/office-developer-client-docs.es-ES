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
ms.openlocfilehash: 6b21d6746baf438af438787d966d9af886d4a74f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425473"
---
# <a name="setting-a-table-position-with-a-filter"></a><span data-ttu-id="42f4d-103">Establecer una posición de tabla con un filtro</span><span class="sxs-lookup"><span data-stu-id="42f4d-103">Setting a Table Position with a Filter</span></span>

  
  
<span data-ttu-id="42f4d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42f4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42f4d-105">Los usuarios de la tabla pueden mover el cursor a una fila que coincida con un conjunto de criterios de filtro.</span><span class="sxs-lookup"><span data-stu-id="42f4d-105">Table users can move the cursor to a row that matches a set of filter criteria.</span></span> <span data-ttu-id="42f4d-106">Los filtros pueden basarse en una variedad de directrices, como valores de propiedad de columna, máscaras de bits o subobjetos.</span><span class="sxs-lookup"><span data-stu-id="42f4d-106">Filters can be based on a variety of guidelines such as column property values, bitmasks, or subobjects.</span></span> <span data-ttu-id="42f4d-107">Los filtros se especifican en MAPI mediante una [estructura SRestriction.](srestriction.md)</span><span class="sxs-lookup"><span data-stu-id="42f4d-107">Filters are specified in MAPI using an [SRestriction](srestriction.md) structure.</span></span> 
  
 <span data-ttu-id="42f4d-108">**Para colocar una tabla en la primera fila que coincida con los criterios establecidos en una restricción**</span><span class="sxs-lookup"><span data-stu-id="42f4d-108">**To position a table to the first row that matches the criteria established in a restriction**</span></span>
  
- <span data-ttu-id="42f4d-109">Llame al [método IMAPITable::FindRow.](imapitable-findrow.md)</span><span class="sxs-lookup"><span data-stu-id="42f4d-109">Call the [IMAPITable::FindRow](imapitable-findrow.md) method.</span></span> <span data-ttu-id="42f4d-110">Empezando por la fila representada por un marcador determinado, **FindRow** busca en dirección hacia delante o hacia atrás para buscar una fila que coincida con los criterios especificados en la restricción.</span><span class="sxs-lookup"><span data-stu-id="42f4d-110">Starting with the row represented by a particular bookmark, **FindRow** searches in either a forward or backward direction to locate a row that matches the criteria specified in the restriction.</span></span> <span data-ttu-id="42f4d-111">**FindRow** puede ser útil para implementar una barra de desplazamiento basada en cadenas de caracteres, en lugar de valores fraccionados.</span><span class="sxs-lookup"><span data-stu-id="42f4d-111">**FindRow** can be useful for implementing a scroll bar that is based on character strings, instead of fractional values.</span></span> <span data-ttu-id="42f4d-112">Por ejemplo, un cliente puede llamar a la implementación de MAPI de **FindRow** al buscar en la libreta de direcciones integrada para permitir que un usuario, al escribir uno o más caracteres, busque el primer nombre que comienza con los caracteres especificados.</span><span class="sxs-lookup"><span data-stu-id="42f4d-112">For example, a client can call MAPI's implementation of **FindRow** when searching through the integrated address book to enable a user, by entering one or more characters, to locate the first name that begins with the specified characters.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="42f4d-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="42f4d-113">See also</span></span>



[<span data-ttu-id="42f4d-114">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="42f4d-114">MAPI Tables</span></span>](mapi-tables.md)

