---
title: Tipos y los identificadores de propiedad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 7f31162e669af6efaf9e935c7c400d105c1321c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820445"
---
# <a name="property-identifiers-and-types"></a><span data-ttu-id="6ee49-103">Tipos y los identificadores de propiedad</span><span class="sxs-lookup"><span data-stu-id="6ee49-103">Property Identifiers and Types</span></span>

  
  
<span data-ttu-id="6ee49-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6ee49-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6ee49-105">Todas las propiedades MAPI se representan mediante las etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="6ee49-105">All MAPI properties are represented by property tags.</span></span> <span data-ttu-id="6ee49-106">Una etiqueta de propiedad es un valor entero sin signo de 32 bits que contiene el identificador de la propiedad en la alta pedidos 16 bits y el tipo de propiedad en la baja pedidos 16 bits.</span><span class="sxs-lookup"><span data-stu-id="6ee49-106">A property tag is a 32-bit unsigned integer value that contains the property's identifier in the high order 16 bits and the property's type in the low order 16 bits.</span></span> <span data-ttu-id="6ee49-107">Etiquetas de propiedad para todas las propiedades definidas por MAPI se incluyen en el archivo de encabezado mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="6ee49-107">Property tags for all of the properties defined by MAPI are included in the mapitags.h header file.</span></span>
  
<span data-ttu-id="6ee49-108">Identificadores de propiedad se usan para indicar qué se usa una propiedad y quién es responsable de ella.</span><span class="sxs-lookup"><span data-stu-id="6ee49-108">Property identifiers are used to indicate what a property is used for and who is responsible for it.</span></span> <span data-ttu-id="6ee49-109">Identificadores de propiedad se dividen por MAPI en intervalos; donde se encuentra un identificador en el intervalo indica su uso y la propiedad.</span><span class="sxs-lookup"><span data-stu-id="6ee49-109">Property identifiers are divided by MAPI into ranges; where an identifier falls in the range indicates its use and ownership.</span></span> 
  
<span data-ttu-id="6ee49-110">Tipos de propiedad se usan para indicar el formato de datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="6ee49-110">Property types are used to indicate the format of the property's data.</span></span> <span data-ttu-id="6ee49-111">MAPI define todos los tipos válidos.</span><span class="sxs-lookup"><span data-stu-id="6ee49-111">MAPI defines all of the valid types.</span></span> <span data-ttu-id="6ee49-112">Los clientes y proveedores de servicios de creación de nuevas propiedades deben usar uno de estos tipos.</span><span class="sxs-lookup"><span data-stu-id="6ee49-112">Clients and service providers creating new properties must use one of these types.</span></span> <span data-ttu-id="6ee49-113">Todos los tipos de propiedad se incluyen en el archivo de encabezado mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="6ee49-113">All of the property types are included in the mapidefs.h header file.</span></span>
  

