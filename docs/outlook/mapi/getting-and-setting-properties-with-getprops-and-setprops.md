---
title: Obtener y establecer propiedades con GetProps y SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6b54be711d8c33648d211e480c6a00ee92755108
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575570"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a><span data-ttu-id="ddb53-103">Obtener y establecer propiedades con GetProps y SetProps</span><span class="sxs-lookup"><span data-stu-id="ddb53-103">Getting and setting properties with GetProps and SetProps</span></span>
 
<span data-ttu-id="ddb53-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ddb53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ddb53-105">Siempre que sea posible, vuelva a intentar recuperar o modificar una propiedad con los métodos [IMAPIProp::GetProps](imapiprop-getprops.md) y [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="ddb53-105">Whenever possible, try to retrieve or modify a property with the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="ddb53-106">A menos que la propiedad con que trabaja es muy grande, estos métodos deben ser adecuados.</span><span class="sxs-lookup"><span data-stu-id="ddb53-106">Unless the property you are working with is very large, these methods should be adequate.</span></span> <span data-ttu-id="ddb53-107">La otra alternativa consiste en leer o escribir en un objeto stream con la interfaz [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ddb53-107">The other alternative is to read from or write to a stream with the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="ddb53-108">Secuencias de pueden controlar correctamente las propiedades muy grandes, pero son un mayor consumo de recursos debido a que requieren que las bibliotecas COM.</span><span class="sxs-lookup"><span data-stu-id="ddb53-108">Streams can handle very large properties successfully, but they are a greater drain on resources because they require the COM libraries.</span></span> <span data-ttu-id="ddb53-109">Use la interfaz **IStream** sólo después de que se produce un error en la llamada a **IMAPIProp::GetProps** o **IMAPIProp::SetProps** .</span><span class="sxs-lookup"><span data-stu-id="ddb53-109">Use the **IStream** interface only after your call to **IMAPIProp::GetProps** or **IMAPIProp::SetProps** fails.</span></span> 
  

