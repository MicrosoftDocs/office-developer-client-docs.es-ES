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
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299401"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a><span data-ttu-id="8afa1-103">Obtener y establecer propiedades con GetProps y SetProps</span><span class="sxs-lookup"><span data-stu-id="8afa1-103">Getting and setting properties with GetProps and SetProps</span></span>
 
<span data-ttu-id="8afa1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8afa1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8afa1-105">Siempre que sea posible, intente recuperar o modificar una propiedad con los métodos [IMAPIProp:: GetProps](imapiprop-getprops.md) y [IMAPIProp:: SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="8afa1-105">Whenever possible, try to retrieve or modify a property with the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="8afa1-106">A menos que la propiedad con la que trabaja sea muy grande, estos métodos deben ser adecuados.</span><span class="sxs-lookup"><span data-stu-id="8afa1-106">Unless the property you are working with is very large, these methods should be adequate.</span></span> <span data-ttu-id="8afa1-107">La otra alternativa es leer o escribir en una secuencia con la interfaz [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8afa1-107">The other alternative is to read from or write to a stream with the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="8afa1-108">Las secuencias pueden administrar las propiedades muy grandes correctamente, pero son un mayor consumo de recursos porque requieren las bibliotecas COM.</span><span class="sxs-lookup"><span data-stu-id="8afa1-108">Streams can handle very large properties successfully, but they are a greater drain on resources because they require the COM libraries.</span></span> <span data-ttu-id="8afa1-109">Use la interfaz **IStream** solo después de que se produzca un error en la llamada a **IMAPIProp:: GetProps** o **IMAPIProp:: SetProps** .</span><span class="sxs-lookup"><span data-stu-id="8afa1-109">Use the **IStream** interface only after your call to **IMAPIProp::GetProps** or **IMAPIProp::SetProps** fails.</span></span> 
  

