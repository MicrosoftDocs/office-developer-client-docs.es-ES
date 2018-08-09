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
ms.openlocfilehash: 150f2a55bff4188c1f692de8276ed869bcf66c3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816920"
---
# <a name="getting-and-setting-multiple-properties"></a><span data-ttu-id="16a59-103">Obtener y establecer varias propiedades</span><span class="sxs-lookup"><span data-stu-id="16a59-103">Getting and setting multiple properties</span></span>

<span data-ttu-id="16a59-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="16a59-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="16a59-105">Para obtener y establecer propiedades tantos como sea posible con el menor número de llamadas, remotas actividad es reducida y se reduce la sobrecarga que implica con cada propiedad.</span><span class="sxs-lookup"><span data-stu-id="16a59-105">By getting and setting as many properties as possible with the least number of calls, remote activity is curtailed and the overhead involved with each property is reduced.</span></span> <span data-ttu-id="16a59-106">Aunque los proveedores de servicios intentan recopilar propiedades antes de realizar una llamada a procedimiento remoto para la recuperación o modificación, puede optimizar este esfuerzo solicitando varias propiedades para empezar.</span><span class="sxs-lookup"><span data-stu-id="16a59-106">Although service providers try to collect properties before making a remote procedure call for retrieval or modification, you can optimize this effort by requesting multiple properties to begin with.</span></span>
  
<span data-ttu-id="16a59-107">Por ejemplo, si trabaja con listas de enrutamiento que describen a los destinatarios futuros con las propiedades con nombre que pertenecen a conjuntos de propiedades determinado, proceso de todos los destinatarios con dos llamadas.</span><span class="sxs-lookup"><span data-stu-id="16a59-107">For example, if you work with routing lists that describe future recipients with named properties belonging to particular property sets, process all of the recipients with two calls.</span></span> <span data-ttu-id="16a59-108">Utilice una llamada a [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para recuperar los identificadores de todas las propiedades del destinatario y la otra llamada a [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar todos los valores.</span><span class="sxs-lookup"><span data-stu-id="16a59-108">Use one call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to retrieve the identifiers for all of the recipient properties and the other call to [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve all of the values.</span></span> <span data-ttu-id="16a59-109">La alternativa, realizar una llamada a **a GetIDsFromNames** seguido de una llamada a **GetProps** para cada destinatario, es mucho menos eficaz.</span><span class="sxs-lookup"><span data-stu-id="16a59-109">The alternative, making a call to **GetIDsFromNames** followed by a call to **GetProps** for each recipient, is much less efficient.</span></span> 
  

