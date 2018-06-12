---
title: Agrupar y la restricción de las tablas de proveedores de almacén de mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 33c76cdd0e7850f82949349ac2e5bb0dd4e056ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816926"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a><span data-ttu-id="4e872-103">Agrupar y la restricción de las tablas de proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="4e872-103">Grouping and Restricting Tables in Message Store Providers</span></span>

  
  
<span data-ttu-id="4e872-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4e872-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4e872-105">Con frecuencia, las aplicaciones cliente de permiten a los usuarios cierto control sobre cómo se muestra el contenido de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="4e872-105">Client applications frequently allow users some control over how the contents of a folder are displayed.</span></span> <span data-ttu-id="4e872-106">Normalmente, un usuario puede elegir para que los mensajes se agrupan según el valor de una o varias propiedades del mensaje, o puede optar por excluir los mensajes que coinciden con determinados criterios.</span><span class="sxs-lookup"><span data-stu-id="4e872-106">Typically, a user can choose to have messages grouped according to the value of one or more message properties, or can choose to exclude messages that match certain criteria.</span></span> <span data-ttu-id="4e872-107">Esto se realiza mediante la [IMAPITable: IUnknown](imapitableiunknown.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="4e872-107">This is done by using the [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span></span> <span data-ttu-id="4e872-108">Las aplicaciones cliente pueden restringir las filas devueltas desde la tabla a cualquier criterio especifica el usuario.</span><span class="sxs-lookup"><span data-stu-id="4e872-108">Client applications can restrict the rows returned from the table to whatever criteria the user specifies.</span></span> <span data-ttu-id="4e872-109">Por lo tanto, un mensaje de almacenar las necesidades del proveedor para implementar los métodos **IMAPITable** siguientes.</span><span class="sxs-lookup"><span data-stu-id="4e872-109">Therefore, a message store provider needs to implement the following **IMAPITable** methods.</span></span> 
  
|<span data-ttu-id="4e872-110">IMAPITable ** (método) **</span><span class="sxs-lookup"><span data-stu-id="4e872-110">****IMAPITable** method**</span></span>|<span data-ttu-id="4e872-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4e872-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e872-112">Elemento IMAPITable:: FindRow</span><span class="sxs-lookup"><span data-stu-id="4e872-112">IMAPITable::FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="4e872-113">Devuelve la tabla de las filas que coinciden con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="4e872-113">Returns table rows that match the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="4e872-114">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="4e872-114">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="4e872-115">Devuelve el conjunto de columnas en una tabla o el conjunto de columnas usados actualmente.</span><span class="sxs-lookup"><span data-stu-id="4e872-115">Returns the set of columns in a table or the set of currently used columns.</span></span>  <br/> |
|[<span data-ttu-id="4e872-116">IMAPITable:: QueryRows</span><span class="sxs-lookup"><span data-stu-id="4e872-116">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="4e872-117">Devuelve una o varias filas de una tabla, a partir de una posición determinada.</span><span class="sxs-lookup"><span data-stu-id="4e872-117">Returns one or more rows from a table, starting from a given position.</span></span>  <br/> |
|[<span data-ttu-id="4e872-118">IMAPITable:: Restrict</span><span class="sxs-lookup"><span data-stu-id="4e872-118">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="4e872-119">Se aplica una restricción a una tabla para que las llamadas subsiguientes a **FindRow** devolverán sólo las filas que coinciden con la restricción.</span><span class="sxs-lookup"><span data-stu-id="4e872-119">Applies a restriction to a table so that subsequent calls to **FindRow** return only rows that match the restriction.</span></span>  <br/> |
|[<span data-ttu-id="4e872-120">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="4e872-120">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="4e872-121">Especifica las columnas que se deben devolver cuando se recuperan las filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="4e872-121">Specifies which columns should be returned when rows are retrieved from the table.</span></span>  <br/> |
   
<span data-ttu-id="4e872-122">Restricciones pueden ser difíciles implementar; Para obtener más información, vea [Acerca de las restricciones](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="4e872-122">Restrictions can be complex to implement; for more information, see [About Restrictions](about-restrictions.md).</span></span> <span data-ttu-id="4e872-123">Para obtener más información acerca de cómo implementar las tablas, vea [Tablas de MAPI](mapi-tables.md).</span><span class="sxs-lookup"><span data-stu-id="4e872-123">For more information about implementing tables, see [MAPI Tables](mapi-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e872-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="4e872-124">See also</span></span>



[<span data-ttu-id="4e872-125">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="4e872-125">Message Store Features</span></span>](message-store-features.md)

