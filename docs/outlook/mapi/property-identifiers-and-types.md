---
title: Identificadores y tipos de propiedad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: caba60b7059d1c1f8f0440aeb55abb88801fbc9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437220"
---
# <a name="property-identifiers-and-types"></a><span data-ttu-id="22cbc-103">Identificadores y tipos de propiedad</span><span class="sxs-lookup"><span data-stu-id="22cbc-103">Property Identifiers and Types</span></span>

  
  
<span data-ttu-id="22cbc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22cbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22cbc-105">Todas las propiedades MAPI se representan mediante etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="22cbc-105">All MAPI properties are represented by property tags.</span></span> <span data-ttu-id="22cbc-106">Una etiqueta de propiedad es un valor entero sin signo de 32 bits que contiene el identificador de la propiedad en los 16 bits de orden superior y el tipo de la propiedad en los 16 bits de orden bajo.</span><span class="sxs-lookup"><span data-stu-id="22cbc-106">A property tag is a 32-bit unsigned integer value that contains the property's identifier in the high order 16 bits and the property's type in the low order 16 bits.</span></span> <span data-ttu-id="22cbc-107">Las etiquetas de propiedad de todas las propiedades definidas por MAPI se incluyen en el archivo de encabezado mapitags. h.</span><span class="sxs-lookup"><span data-stu-id="22cbc-107">Property tags for all of the properties defined by MAPI are included in the mapitags.h header file.</span></span>
  
<span data-ttu-id="22cbc-108">Los identificadores de propiedad se usan para indicar para qué se usa una propiedad y quién es responsable de la misma.</span><span class="sxs-lookup"><span data-stu-id="22cbc-108">Property identifiers are used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="22cbc-109">Los identificadores de propiedad se dividen en rangos mediante MAPI; donde un identificador cae en el intervalo indica su uso y propiedad.</span><span class="sxs-lookup"><span data-stu-id="22cbc-109">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="22cbc-110">Los tipos de propiedad se usan para indicar el formato de los datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="22cbc-110">Property types are used to indicate the format of the property's data.</span></span> <span data-ttu-id="22cbc-111">MAPI define todos los tipos válidos.</span><span class="sxs-lookup"><span data-stu-id="22cbc-111">MAPI defines all of the valid types.</span></span> <span data-ttu-id="22cbc-112">Los clientes y los proveedores de servicios que crean nuevas propiedades deben usar uno de estos tipos.</span><span class="sxs-lookup"><span data-stu-id="22cbc-112">Clients and service providers creating new properties must use one of these types.</span></span> <span data-ttu-id="22cbc-113">Todos los tipos de propiedad se incluyen en el archivo de encabezado mapidefs. h.</span><span class="sxs-lookup"><span data-stu-id="22cbc-113">All of the property types are included in the mapidefs.h header file.</span></span>
  

