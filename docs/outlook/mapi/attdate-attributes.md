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
ms.openlocfilehash: ff0cc6b1c17b2ed83d7b0ec0921904763da8624b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567016"
---
# <a name="attdate-attributes"></a><span data-ttu-id="7aecc-103">Atributos attDate</span><span class="sxs-lookup"><span data-stu-id="7aecc-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="7aecc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7aecc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7aecc-105">Todas las propiedades MAPI relativas a las fechas y horas se asignan a los atributos TNEF que tienen el prefijo **attDate** .</span><span class="sxs-lookup"><span data-stu-id="7aecc-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="7aecc-106">Estos se codifican como estructuras **DTR** .</span><span class="sxs-lookup"><span data-stu-id="7aecc-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="7aecc-107">Las fechas y horas para los atributos de los datos adjuntos se codifican como así como las estructuras **DTR** .</span><span class="sxs-lookup"><span data-stu-id="7aecc-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="7aecc-108">Todas las propiedades MAPI relativas a las fechas y horas se asignan a los atributos TNEF que tienen el prefijo **attDate** .</span><span class="sxs-lookup"><span data-stu-id="7aecc-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="7aecc-109">Estos se codifican como estructuras **DTR** .</span><span class="sxs-lookup"><span data-stu-id="7aecc-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="7aecc-110">Las fechas y horas para los atributos de los datos adjuntos se codifican como así como las estructuras **DTR** .</span><span class="sxs-lookup"><span data-stu-id="7aecc-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="7aecc-111">Una estructura **DTR** es muy similar a la estructura **SYSTEMTIME** definida en los archivos de encabezado de Win32.</span><span class="sxs-lookup"><span data-stu-id="7aecc-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="7aecc-112">La estructura **DTR** está codificada en la secuencia TNEF como bytes **sizeof(DTR)** empezando por el primer miembro de la estructura.</span><span class="sxs-lookup"><span data-stu-id="7aecc-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="7aecc-113">La estructura **DTR** se define en el TNEF. Archivo de encabezado H.</span><span class="sxs-lookup"><span data-stu-id="7aecc-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

