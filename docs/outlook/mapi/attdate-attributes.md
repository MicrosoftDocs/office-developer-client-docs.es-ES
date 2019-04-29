---
title: Atributos attDate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b7c1ce8d0338a2bda63a276628bdd6e8be3b8eb1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408281"
---
# <a name="attdate-attributes"></a><span data-ttu-id="1ed9b-103">Atributos attDate</span><span class="sxs-lookup"><span data-stu-id="1ed9b-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="1ed9b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ed9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ed9b-105">Todas las propiedades MAPI relativas a las fechas y horas se asignan a los atributos TNEF que tienen el prefijo **attDate** .</span><span class="sxs-lookup"><span data-stu-id="1ed9b-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="1ed9b-106">Todas están codificadas como estructuras **DTR** .</span><span class="sxs-lookup"><span data-stu-id="1ed9b-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="1ed9b-107">Las fechas y las horas de los atributos de datos adjuntos se codifican también como estructuras **DTR** .</span><span class="sxs-lookup"><span data-stu-id="1ed9b-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="1ed9b-108">Todas las propiedades MAPI relativas a las fechas y horas se asignan a los atributos TNEF que tienen el prefijo **attDate** .</span><span class="sxs-lookup"><span data-stu-id="1ed9b-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="1ed9b-109">Todas están codificadas como estructuras **DTR** .</span><span class="sxs-lookup"><span data-stu-id="1ed9b-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="1ed9b-110">Las fechas y las horas de los atributos de datos adjuntos se codifican también como estructuras **DTR** .</span><span class="sxs-lookup"><span data-stu-id="1ed9b-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="1ed9b-111">Una estructura **DTR** es muy similar a la estructura **SYSTEMTIME** definida en los archivos de encabezado de Win32.</span><span class="sxs-lookup"><span data-stu-id="1ed9b-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="1ed9b-112">La estructura **DTR** se codifica en la secuencia TNEF como bytes **sizeof (DTR)** a partir del primer miembro de la estructura.</span><span class="sxs-lookup"><span data-stu-id="1ed9b-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="1ed9b-113">La estructura **DTR** se define en la TNEF. H archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="1ed9b-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

