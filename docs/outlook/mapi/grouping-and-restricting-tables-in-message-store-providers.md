---
title: Agrupación y restricción de tablas en proveedores de almacén de mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8a45a9fd0d40c16d110fd52be1ac1117e1dd4d04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428987"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a><span data-ttu-id="35446-103">Agrupación y restricción de tablas en proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="35446-103">Grouping and Restricting Tables in Message Store Providers</span></span>

  
  
<span data-ttu-id="35446-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35446-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35446-105">Con frecuencia, las aplicaciones cliente permiten a los usuarios tener cierto control sobre cómo se muestra el contenido de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="35446-105">Client applications frequently allow users some control over how the contents of a folder are displayed.</span></span> <span data-ttu-id="35446-106">Normalmente, un usuario puede elegir que los mensajes se a agrupan según el valor de una o más propiedades de mensaje, o puede optar por excluir los mensajes que coinciden con ciertos criterios.</span><span class="sxs-lookup"><span data-stu-id="35446-106">Typically, a user can choose to have messages grouped according to the value of one or more message properties, or can choose to exclude messages that match certain criteria.</span></span> <span data-ttu-id="35446-107">Esto se realiza mediante la interfaz [IMAPITable : IUnknown.](imapitableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="35446-107">This is done by using the [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span></span> <span data-ttu-id="35446-108">Las aplicaciones cliente pueden restringir las filas devueltas de la tabla a los criterios que especifique el usuario.</span><span class="sxs-lookup"><span data-stu-id="35446-108">Client applications can restrict the rows returned from the table to whatever criteria the user specifies.</span></span> <span data-ttu-id="35446-109">Por lo tanto, un proveedor de almacenamiento de mensajes debe implementar los **siguientes métodos IMAPITable.**</span><span class="sxs-lookup"><span data-stu-id="35446-109">Therefore, a message store provider needs to implement the following **IMAPITable** methods.</span></span> 
  
|<span data-ttu-id="35446-110">Método IMAPITable\*\*</span><span class="sxs-lookup"><span data-stu-id="35446-110">\*\*\*\*IMAPITable\*\* method\*\*</span></span>|<span data-ttu-id="35446-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="35446-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="35446-112">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="35446-112">IMAPITable::FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="35446-113">Devuelve filas de tabla que coinciden con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="35446-113">Returns table rows that match the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="35446-114">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="35446-114">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="35446-115">Devuelve el conjunto de columnas de una tabla o el conjunto de columnas usadas actualmente.</span><span class="sxs-lookup"><span data-stu-id="35446-115">Returns the set of columns in a table or the set of currently used columns.</span></span>  <br/> |
|[<span data-ttu-id="35446-116">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="35446-116">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="35446-117">Devuelve una o más filas de una tabla, empezando desde una posición determinada.</span><span class="sxs-lookup"><span data-stu-id="35446-117">Returns one or more rows from a table, starting from a given position.</span></span>  <br/> |
|[<span data-ttu-id="35446-118">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="35446-118">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="35446-119">Aplica una restricción a una tabla para que las llamadas posteriores a **FindRow** devuelvan solo las filas que coincidan con la restricción.</span><span class="sxs-lookup"><span data-stu-id="35446-119">Applies a restriction to a table so that subsequent calls to **FindRow** return only rows that match the restriction.</span></span>  <br/> |
|[<span data-ttu-id="35446-120">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="35446-120">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="35446-121">Especifica qué columnas se deben devolver cuando se recuperan filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="35446-121">Specifies which columns should be returned when rows are retrieved from the table.</span></span>  <br/> |
   
<span data-ttu-id="35446-122">Las restricciones pueden ser complejas de implementar; para obtener más información, vea [Acerca de las restricciones](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="35446-122">Restrictions can be complex to implement; for more information, see [About Restrictions](about-restrictions.md).</span></span> <span data-ttu-id="35446-123">Para obtener más información acerca de la implementación de tablas, vea [Tablas MAPI](mapi-tables.md).</span><span class="sxs-lookup"><span data-stu-id="35446-123">For more information about implementing tables, see [MAPI Tables](mapi-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="35446-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="35446-124">See also</span></span>



[<span data-ttu-id="35446-125">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="35446-125">Message Store Features</span></span>](message-store-features.md)

