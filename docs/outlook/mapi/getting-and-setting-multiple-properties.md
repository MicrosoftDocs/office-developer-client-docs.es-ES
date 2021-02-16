---
title: Obtener y establecer varias propiedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: dd25751978eb036531238e6372e35934b3ec145a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432264"
---
# <a name="getting-and-setting-multiple-properties"></a><span data-ttu-id="11ea6-103">Obtener y establecer varias propiedades</span><span class="sxs-lookup"><span data-stu-id="11ea6-103">Getting and setting multiple properties</span></span>

<span data-ttu-id="11ea6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11ea6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11ea6-105">Al obtener y establecer tantas propiedades como sea posible con el menor número de llamadas, la actividad remota se reduce y se reduce la sobrecarga que implica cada propiedad.</span><span class="sxs-lookup"><span data-stu-id="11ea6-105">By getting and setting as many properties as possible with the least number of calls, remote activity is curtailed and the overhead involved with each property is reduced.</span></span> <span data-ttu-id="11ea6-106">Aunque los proveedores de servicios intentan recopilar propiedades antes de realizar una llamada de procedimiento remoto para la recuperación o modificación, puede optimizar este esfuerzo solicitando varias propiedades para empezar.</span><span class="sxs-lookup"><span data-stu-id="11ea6-106">Although service providers try to collect properties before making a remote procedure call for retrieval or modification, you can optimize this effort by requesting multiple properties to begin with.</span></span>
  
<span data-ttu-id="11ea6-107">Por ejemplo, si trabaja con listas de enrutamiento que describen destinatarios futuros con propiedades con nombre pertenecientes a conjuntos de propiedades concretos, procese a todos los destinatarios con dos llamadas.</span><span class="sxs-lookup"><span data-stu-id="11ea6-107">For example, if you work with routing lists that describe future recipients with named properties belonging to particular property sets, process all of the recipients with two calls.</span></span> <span data-ttu-id="11ea6-108">Use una llamada a [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para recuperar los identificadores de todas las propiedades del destinatario y la otra llamada a [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar todos los valores.</span><span class="sxs-lookup"><span data-stu-id="11ea6-108">Use one call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to retrieve the identifiers for all of the recipient properties and the other call to [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve all of the values.</span></span> <span data-ttu-id="11ea6-109">La alternativa, realizar una llamada a **GetIDsFromNames** seguida de una llamada a **GetProps** para cada destinatario, es mucho menos eficaz.</span><span class="sxs-lookup"><span data-stu-id="11ea6-109">The alternative, making a call to **GetIDsFromNames** followed by a call to **GetProps** for each recipient, is much less efficient.</span></span> 
  

